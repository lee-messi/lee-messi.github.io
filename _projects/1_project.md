---
layout: page
title: Homogeneity Bias in Artifical Intelligence
description: 
img: 
importance: 1
category: work
related_publications: true
---

# The Outgroup Homogeneity Effect

Social psychologists have long studied a phenomenon referred to as the *outgroup homogeneity effect*. This phenomenon refers to a tendency of individuals to perceive members of *outgroups* as more homogeneous than members of *ingroups*. Here, ingroup refers to the group that someone identifies with while outgroup refers to the group that one *does not* identify with. For example, as a student of Washington University in St. Louis, I would identify other students at WashU as my ingroup whereas I would identify students at other schools as my outgroup, and according to the *outgroup homogeneity effect*, I have the tendency to perceive students at other schools as more homogeneous and less diverse than students at WashU. 

A number of explanations explain this phenomenon. One is *contact*. Naturally, we are more likely to come into contact with ingroup members than outgroup members. For exmaple, I am more likely to come across different students at WashU, taking classes or going to and from the lab, than I am to come across students at other schools. Because I come across more students at WashU, of different majors, looks, styles, personality ... etc., I can perceive them as more diverse. On the other hand, I am more likely to generalize based on the limited observations I've made, if any, about other groups, and perceive them that way. 

Another explanation has to do with the *social-categorization theory*. The theory posits that individuals tend to classify themselves into groups and that the dynamic between these groups affects our behavior towards others. For example, when we come into contact with an outgroup member, we are more likely to pay attention to the difference between gorups as opposed to difference *within* groups. This results in a more heterogeneous perception of the outgroup. On the other hand, when coming into contact with an ingroup member, we are more likely to focus on the *within* group differences, which leads to a more heterogeneous perception of the ingroup. 

# Outgroup Homogeneity Effect in the Context of Group Power/Status

The outgroup homogeneity effect is specific to the intergroup context (i.e., the ingroup-outgroup context), but the perception of a group as more or less homogeneous extends to other contexts as well. The context that my research focuses on is *group power*: if power affects the homogeneity that we associate with a group. What's interesting is that in the group power context, we observe unique patterns that deviate from the outgroup homogeneity effect. That is, according to the outgroup homogeneity effect, the group in power, say the racial majority in the United States -- White Americans -- are likely to perceive members of their outgroup -- racial minority groups as more homogeneous. The opposite is to be expected for racial minority group members: they would perceive members of their outgroup -- White Americans -- as more homogeneous. 

Surprisingly, research finds that only half of this is true. The group in power exhibits the outgroup homogeneity effect, but the group not in power, or the socially subordiante group, tends to perceive members of their ingroup as more homogeneous than members of their outgroup. These two, altogether, point to a consistent direction where members of both the racial majority and minority perceive members of the racial minority as more homogeneous. This phenomenon is what we refer to as **homogeneity bias** in my work. 

There is a number of explanations for why this may be. One explanation, which also relates to *social categorization theory*, is that groups not in power may be motivated to boost intragroup solidarity by focusing on similarities shared within the group. Because they focus on intragroup similarity, they focus less on intragroup differences, and hence perceive the ingroup as more homogeneous. Another explanation is that the outcome of groups not in power depend on the resources of those that are in power, and hence groups not in power are motivated to focus on differentiating traits of those in power. Hence, groups not in power are more likely to focus on differences within their outgroup, which leads to them perceiving their ingroup as more homogeneous. Another interesting explanation is that those in power have access to more broad and diverse real-world outcomes whereas those not in power are constrained to a path they need power and resources to break away from. This real-world disparity in diversity of outcomes also affects perceptions of homogeneity. 

# Why does Homogeneity Bias Matter? 

One outstanding implication of homogeneity bias is that perceiving a group as more homogeneous leads to greater stereotyping, prejudice, and discrimination. When we perceive a group as being more heterogeneous, it also means that we are more likely to associate them with stereotypic traits. These observations have led to social psychological interventions where, in the intervention, individuals are made salient about the heterogeneity of the target group (e.g., their subgroups), which in turn reduces negative prejudice and discrimination against the target group (). 

# Bias in Artifical Intelligence Systems

One of the biggest phenomena that happened during my PhD is Artifical Intelligence (AI), particularly Large Language Models (LLMs) and, increasingly, multimodal models. What I find most interesting about this explosion is that LLMs and the like tend to reproduce human-like biases. For example, GPT-3, the LLM that started to catch people's attention back in 2021, when writing stories about gender groups, reproduce gender stereotypes - they associate male characters with sports, war, crime, and politics, and associate female characters with body parts, family, and emotions (Lucy & Bamman, 2021). 

My research was motivated by the simple question of: if AI sytems reproduce human-like biases, like stereotyping, would they also reproduce homogeneity bias? Would they represent socially subordinate groups as more homogeneous compared to the dominant groups? The approach to finding an answer to this question was pretty straightforward. We asked an LLM - ChatGPT - to generate a variety of text about racial/ethnic and gender groups, and we measured homogeneity of the generated text. 

# Measuring and Comparing Homogeneity of Text

At first, it wasn't clear to us how we would quantify homogeneity of text. For one, we had to figure out what homogeneity of text meant. Would we consider texts to be homogeneous if they used the same words? What if the texts used the same words but meant the exact opposite things? What if the texts used the same prepositions (e.g., for, to, in) and/or articles (e.g., the, a), words that don't contribute much to the meaning of the sentence? To ensure that the measure of homogeneity would capture similarity in meaning, we decided to use sentence embeddings - vector representations of text that encode both semantic and syntactic information of text. To measure *homogeneity* of sentence embeddings, we measured pairwise cosine similarity of the sentence embeddings, a measure of distance between two numeric vectors. The intuition was that if a collection of texts is more homogeneous than a collection of others, they would share significantly higher (pairwise) cosine similarity values. 

We had measured pairwise cosine similarity values between texts generated for individual prompts. These prompts were specific to race/ethnicity, gender, and text format (e.g., story, biography, self-introduction). On one hand, we wanted to compare cosine similarity values between racial/ethnic and gender groups, but we also wanted to account for the fact that different text formats would share different baseline cosine similarity values. This was based on a simple observation that certain text formats, by default, may be more similar to each other than others. For example, self-introductions tend to contain similar content (e.g., name, job) whereas stories may be more flexible and creative. 

# Large Language Models Represent Socially Subordinate Groups as More Homogeneous

We find that texts generated for racial/ethnic minorities (i.e., African, Asian, and Hispanic Americans) and women share significantly higher cosine similarity values compared to White Americans and men {% cite lee_large_2024 %}. These differences were greater within racial/ethnic groups compared to that within gender groups. Furthermore, the effect of gender was generally consistent within individual racial/ethnic groups, with it being largest within Hispanic Americans. These findings were generally consistent across measurement strategies, measurement strategies referring to the different encoder models used to represent the generated text into numeric vector representations. 

<div class="row">
    <div class="col-sm mt-6 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bert2_race.pdf" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-6 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bert2_interaction.pdf" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Standardized cosine similarity values of all eight intersectional groups (left) and four racial/ethnic groups (right). Error bars were omitted as confidence intervals were all smaller than 0.001.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
