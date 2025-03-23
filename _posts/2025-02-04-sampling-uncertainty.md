---
layout: post
title: Homogeneity Bias as Differential Sampling Uncertainty
date: 2025-02-04 00:00:00
description: Introduction to a new paper
tags: homogeneity-bias
categories: research
---

Recently, I came across an interesting paper investigating how regularizing attention weights could encourage BERT-like models to consider broader token contexts when constructing token-level representations thereby mitigating social biases (Attanasio et al., 2022). That's quite technical, so let me walk you through what it means in simpler terms.

## The Connection between Attention and Bias

Think of attention in NLP models like a spotlight. When a model processes a word (token), it shines this spotlight on other words in the context to understand its meaning. For example, when processing the word "doctor," traditional models might shine a very bright spotlight on words like "he" and a dimmer one on "she" - because that's the pattern they learned from training data.

The key idea behind attention regularization is to intentionally diffuse this spotlight–instead of having intense focus on specific gender-associated words, we want the model to distribute its attention more evenly. Here's a way to think about it:

In a normal setup, when processing "doctor", the attention weights might look like:

- "he": 0.7
- "she": 0.2
- non-gendered pronouns: 0.1

With regularization, we push for more balanced attention:

- "he": 0.4
- "she": 0.4
- non-gendered pronouns: 0.2

By enforcing this more uniform distribution of attention, we reduce the model's tendency to strongly associate certain professions with specific genders. It's like telling the model: "Don't jump to conclusions about gender when you're thinking about occupations."

## How it Relates to Homogeneity Bias

This work on regularizing attention weights to mitigate social bias led me to consider homogeneity bias from a new angle. What if homogeneity bias in language models manifests from how these models sample tokens during inference? Specifically, when generating text about marginalized groups, the token sampling distribution might become more deterministic, focusing on a narrower set of possible next words.

{% include figure.liquid loading="eager" path="assets/img/2025-02-04-sampling-uncertainty/study_design.png" class="img-fluid rounded z-depth-1" %}

We tested this idea using Vision-Language Models as our experimental setup. We asked these models to generate stories about images showing different racial and gender groups, then carefully tracked how the models made their word choices. To measure this scientifically, we used three different metrics: entropy, perplexity, and probability of differentiation. These metrics helped us understand if the model was more predictable when writing about certain groups versus others-similar to how a recommendation system might fall back on popular, safe suggestions when it has limited data about a user's preferences.

## Results

Our initial analysis with GPT-4 Turbo revealed a consistent pattern: when generating text, the model showed significantly lower uncertainty in its word choices when writing about Black Americans and women compared to White Americans and men. This pattern held true across all 50 token positions we analyzed.

{% include figure.liquid loading="eager" path="assets/img/2025-02-04-sampling-uncertainty/race.jpg" class="img-fluid rounded z-depth-1" %}

To verify whether this pattern was unique to GPT-4 Turbo, we expanded our analysis to include three additional models: GPT-4o mini, Llama-3.2, and Ovis-1.6. Llama-3.2 exhibited similar patterns to GPT-4 Turbo, while GPT-4o mini and Ovis-1.6 either showed no significant differences or displayed opposite patterns in their token sampling behavior.

{% include figure.liquid loading="eager" path="assets/img/2025-02-04-sampling-uncertainty/race_position.jpg" class="img-fluid rounded z-depth-1" %}

The visualizations above demonstrate consistently lower measures across token positions for Black Americans compared to White Americans, indicating more deterministic token sampling distributions for Black Americans.

## The Significance of this Work

Our approach offers a new way to understand homogeneity bias in language models by looking directly at how these models make word choices during text generation. Previous methods relied on using encoder models to analyze the final generated text, but these methods shared a fatal limitation: these encoder models might share the same biases as the models being studied, making it harder to isolate different sources of bias.

By examining token sampling distributions during inference, we get a more direct window into how these models actually behave when generating text. Rather than looking at the end product, we're observing the model's decision-making process in real-time – specifically, how certain or uncertain it is when choosing words for different groups. This mechanistic approach helps us pinpoint where and how homogeneity bias manifests in the generation process, opening new possibilities for addressing these biases at their source.

### References

Lee, M. H. J., & Jeon, S. (2025). Homogeneity Bias as Differential Sampling Uncertainty in Language Models (arXiv:2501.19337). arXiv. https://doi.org/10.48550/arXiv.2501.19337

Attanasio, G., Nozza, D., Hovy, D., & Baralis, E. (2022). Entropy-based Attention Regularization Frees Unintended Bias Mitigation from Lists (arXiv:2203.09192). arXiv. https://doi.org/10.48550/arXiv.2203.09192
