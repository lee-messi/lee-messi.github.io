---
layout: post
title: homogeneity bias in artificial intelligence
date: 2025-01-08 00:00:00
description: a short blog post about my research on homogeneity bias
# tags: research
categories: research
---

This blog post introduces my research at the intersection of Social Psychology and Artificial Intelligence. While AI might be familiar to many through recent developments like ChatGPT, the social psychology aspects might be less known. Let me walk you through how these fields connect, starting with a simple classroom example.

## Understanding Social Psychology Through a Classroom

Imagine walking into a classroom of 20 students on the first day of school. You're surrounded by unfamiliar faces, feeling slightly awkward and anxious. As the semester progresses, you work on group projects and play together during recess. Gradually, that initial awkwardness fades as you form friendships. This transformation - how social interactions shape our thoughts, feelings, and behaviors - is what social psychologists study.

## How Groups Form and Divide

In this classroom, students naturally split into groups. Let's say one group loves sports and always plays outside during recess, while another prefers board games indoors. This division, though based simply on interests, can grow stronger over time.

Think about being in the board game group. At first, you might casually invite someone from the sports group to join your game. After several rejections, you start assuming all sports group members wouldn't be interested in board games and decide never to invite anyone again from the sports group. This assumption about an entire group is what we call a *stereotype*. The uncertainty you feel about asking them again is *prejudice*, and eventually choosing not to invite them is *discrimination*.

## Seeing Other Groups as "All the Same"

This classroom dynamic reveals a fascinating pattern: we tend to see members of other groups (outgroups) as more similar to each other than members of our own group (ingroup). As a board game enthusiast, you might think "all the sports kids are alike," while seeing distinct personalities in your fellow board game players.

## Why This Matters

When we start seeing a group as "all the same," something concerning happens. Research shows that this perception leads to more stereotyping, increased negative prejudice, and greater discrimination. Going back to our classroom example, once you start thinking of the sports group as all alike, you might be less likely to notice their individual interests or invite them to join different activities. You might even start making broader assumptions about what they like or don't like, further widening the divide between groups.

## AI Systems Learn From Humans

One of the most fascinating developments during my PhD has been the rise of Artificial Intelligence, particularly Large Language Models like ChatGPT. These models have shown an interesting tendency: they reproduce patterns of human stereotyping. For example, when writing stories about different groups, they often introduce the same gender stereotypes that humans have such as associating men with sports and politics, and women with family and emotions.

This observation led me to a crucial question: if AI systems mirror human patterns of stereotyping, might they also show our tendency to see certain groups as "all the same"? Just as students in our classroom example might view the sports group as more similar to each other than they really are, would AI systems represent some groups as more similar than others?

## Measuring AI Bias

To answer this question, we conducted an experiment. We asked ChatGPT to write various kinds of texts - stories, biographies, and self-introductions - about different racial/ethnic and gender groups. Then came the challenging part: how do we measure if AI sees certain groups as "more similar"?

We approached this by examining how similar the AI's writings were for each group. Think of it like this: if you asked someone to write multiple stories about different board game club members, and the stories were all very similar, you might conclude that this person sees board game club members as "all the same." We did something similar with AI, using computational tools to measure how similar its writings were for different groups.

## What We Found

The results were clear and concerning. Just like humans often view certain groups as more similar to each other, AI systems showed the same pattern. When writing about racial/ethnic minorities and women, the AI's stories were more similar to each other compared to its stories about White Americans and men. This happened even when we specifically asked for diverse, non-stereotypical stories.

Could this simply be because the AI was using similar topics or themes for certain groups? We tested this possibility too. While we did find that AI tended to write about specific themes (like adversity and hardship) more often for some groups, the similarity in writing went beyond just shared topics. Even when writing about the same theme, the AI's descriptions were more similar for certain groups than others.

## Why This Happens

The explanation likely comes from how AI systems learn. These models are trained on massive amounts of human-written text from the internet and other sources. If human writers tend to represent certain groups in more homogeneous ways, the AI learns and reproduces these patterns. It's similar to how students might form overly simplified views of other groups based on limited interactions - AI systems form their "views" based on the limited and potentially biased information in their training data.

## Looking Forward

Our research has recently expanded to study whether these patterns appear when AI systems process facial images. This is particularly important as AI systems become more integrated into our daily lives, from content generation to decision support. Understanding these biases is the first step toward building fairer technology that respects the diversity of groups. 

If you'd like to learn more about this research, you can read our paper "Large Language Models Portray Socially Subordinate Groups as More Homogeneous, Consistent with a Bias Observed in Humans" published in the ACM Conference on Fairness, Accountability, and Transparency 2024 (FAccT '24): https://dl.acm.org/doi/10.1145/3630106.3658975