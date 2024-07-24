---
layout: page
title: Homogeneity Bias in Artifical Intelligence
description: a short introduction to my research
img: 
importance: 1
category: work
related_publications: true
---

Social psychologists have long studied a phenomenon referred to as the *outgroup homogeneity effect*. This phenomenon refers to a tendency of individuals to perceive members of *outgroups* as more homogeneous than members of *ingroups*. Here, ingroup refers to the group that someone identifies with while outgroup refers to the group that one *does not* identify with. For example, as a student of Washington University in St. Louis, I would identify other students at WashU as my ingroup whereas I would identify students at other schools as my outgroup, and according to the *outgroup homogeneity effect*, I have the tendency to perceive students at other schools as more homogeneous and less diverse than students at WashU. 

A number of explanations explain this phenomenon. One is *contact*. Naturally, we are more likely to come into contact with ingroup members than outgroup members. For exmaple, I am more likely to come across different students at WashU, taking classes or going to and from the lab, than I am to come across students at other schools. Because I come across more students at WashU, of different majors, looks, styles, personality ... etc., I can perceive them as more diverse. On the other hand, I am more likely to generalize based on the limited observations I've made, if any, about other groups, and perceive them that way. 

Another explanation has to do with the social identity theory. Social identity theory posits that individuals categorize people into various social groups, identify with groups they belong to, and adopt group membership as part of their self-concept. Minority group members, for example, are more likely to accentuate intragroup solidarity by focusing on common aspects shared within the group, thereby resulting in minority group members being perceived as more homogeneous. 


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
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
