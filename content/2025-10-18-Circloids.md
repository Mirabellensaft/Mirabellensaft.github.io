+++
title = "Circloids"
date = 2024-10-18
description = "A new shape dropped."
extra = {header_img = "/2024-10-18-002.png"}
+++

How do you call a shape that is based on a circle, except that not all points are at a distance *r* from the center? Instead, the distance varies within a set range. I call it a **circloid**.

My goal with this shape was to create a circular form that feels more organic than a perfect circle, as a base to generate more complex shapes. There are so many circular shapes in nature, but they are rarely perfectly round, as surrounding conditions influence their final shape. Think of the growth rings of trees, the shape of mushroom caps, or the petals of flowers. A perfect circle doesn't catch the eye because it's expected. A circloid — a circle that's slightly off-balance — will attract a viewer’s interest.

In the current version, 2/3 of the circloid's circumference is defined by a sine function, while the remaining 1/3 is an arc that closes the shape. Each time a circloid is generated, the starting point’s angle varies, so the distortion doesn’t always occur in the same direction.

How far a circloid deviates from a perfect circle of the same base radius depends on the relationship between frequency, amplitude, and base radius.

**High amplitude and lower frequency** distort the circle in one direction. <br>
**Low amplitude and higher frequency** distort it in multiple directions.

For a smooth circloid, consider the following ratios:

*radius* / *amplitude* should be below 7.0.<br>
*frequency* / *amplitude* should be below 0.5.

<div class="gallery">
<a href="/2024-10-18-003.png" data-ngthumb="/2024-10-18-003.png"></a> 
<a href="/2024-10-18-004.png" data-ngthumb="/2024-10-18-004.png"></a> 
<a href="/2024-10-18-005.png" data-ngthumb="/2024-10-18-005.png"></a> 
<a href="/2024-10-18-006.png" data-ngthumb="/2024-10-18-006.png"></a> 
</div>

In a future version, I can see adding more parameters or predefined options for users to customize the shape exactly as needed.
