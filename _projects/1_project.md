---
layout: page
title: Thrust Vectoring Control
description: Fluidic Thrust Vectoring Control of a Delta Wing UAV
img: assets/img/ftv1.PNG
importance: 1
category: work
related_publications: true
---

This project explored fluidic thrust vectoring (FTV) as an alternative to traditional mechanical control surfaces for unmanned aerial vehicles (UAVs). The work involved both mathematical modeling and computational/experimental validation of fluidic actuation strategies for controlling delta wing configurations.

Key contributions include:

1. Developing analytical and numerical models for FTV-based control of delta wing UAVs.
2. Designing and testing a dynamic experimental rig to validate flow control concepts.
3. Demonstrating that fluidic actuation can generate effective control forces, enabling enhanced maneuverability without the complexity of movable surfaces.

These studies highlighted the potential of FTV for next-generation UAVs, offering reduced mechanical complexity, stealth advantages, and adaptability in both conventional and unconventional flight regimes.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

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

{% endraw %}
