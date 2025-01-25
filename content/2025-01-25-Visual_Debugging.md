+++
title = "Visual Debugging"
date = 2025-01-25
description = "For when you don't want to do the math in your head."
extra = {header_img = "/2025-01-25-001.png"}
+++

Recently I was asked how I debug my generated images, and if I render them often, or if I do all the math in my head. 

The Answer: I always render an image when I run the code. It's just part of the process. Whether I focus on the images or the console output depends on what I'm debugging. It also depends a bit on my mood—sometimes I go for a trial-and-error approach, other times I do the calculations in my head or on paper.

Another thing I do is take the lines I generate apart in [Inkscape](https://inkscape.org/de/). That way, I can check what I’ve actually created and see if it matches what I intended.

<div class="gallery"> <a href="/veranator/nr_000_20250125_192023.png" data-ngthumb="/veranator/nr_000_20250125_192023.png"></a> </div>

I wanted to make a 3x3 grid of concentric squares. For some reason—still unknown at the time—I didn’t get a proper 3x3 grid. Instead, I only got the first square from the first row, the second from the second row, and the third from the third row.

First, I focused on getting the single shape right using the above-mentioned trial-and-error method. I was particularly not in the mood for math in my head that day, this could have been calculated correctly before generating. After this I moved on to debugging the grid. Finally, I worked on the margin. Fixing the grid and margin required changes to the [Sanguine library](https://github.com/Mirabellensaft/Sanguine/tree/main).

The grid didn’t work because of a typo that had been in the library for almost two years. I hadn’t noticed it before because I never accessed that variable in this particular way. I mixed up a [y for an x](https://github.com/Mirabellensaft/Sanguine/blob/8b3098f1f80d6ee69b5257dc3e03a0b9dc31cd94/sanguine_lib/src/resources/layout/grid.rs#L63). As for the margin, that was something I never implemented correctly. It didn’t really matter when plotting, so I never paid much attention to it until now.

To show the process, I have uploaded all the images I rendered along the way — from the starting point, which was based on another piece of code, to the final result. Every time I ran the code, an image was created. If you see multiple images that look the same, it means I didn’t change the code but used the console output instead to figure out where the mistake was. For example, in image 21, you can see how I moved the lines to check what was underneath. 

<div class="gallery">
    <a href="/veranator/nr_000_20250119_171857.png" data-ngthumb="/veranator/nr_000_20250119_171857.png"></a> 
    <a href="/veranator/nr_000_20250119_174558.png" data-ngthumb="/veranator/nr_000_20250119_174558.png"></a>
    <a href="/veranator/nr_000_20250119_174712.png" data-ngthumb="/veranator/nr_000_20250119_174712.png"></a>
    <a href="/veranator/nr_000_20250119_174742.png" data-ngthumb="/veranator/nr_000_20250119_174742.png"></a>
    <a href="/veranator/nr_000_20250119_174811.png" data-ngthumb="/veranator/nr_000_20250119_174811.png"></a>
    <a href="/veranator/nr_000_20250119_174916.png" data-ngthumb="/veranator/nr_000_20250119_174916.png"></a>
    <a href="/veranator/nr_000_20250119_175002.png" data-ngthumb="/veranator/nr_000_20250119_175002.png"></a>
    <a href="/veranator/nr_000_20250119_175114.png" data-ngthumb="/veranator/nr_000_20250119_175114.png"></a>
    <a href="/veranator/nr_000_20250119_175230.png" data-ngthumb="/veranator/nr_000_20250119_175230.png"></a>
    <a href="/veranator/nr_000_20250119_175319.png" data-ngthumb="/veranator/nr_000_20250119_175319.png"></a>
    <a href="/veranator/nr_000_20250119_175401.png" data-ngthumb="/veranator/nr_000_20250119_175401.png"></a>
    <a href="/veranator/nr_000_20250119_175500.png" data-ngthumb="/veranator/nr_000_20250119_175500.png"></a>
    <a href="/veranator/nr_000_20250119_175556.png" data-ngthumb="/veranator/nr_000_20250119_175556.png"></a>
    <a href="/veranator/nr_000_20250119_175624.png" data-ngthumb="/veranator/nr_000_20250119_175624.png"></a>
    <a href="/veranator/nr_000_20250119_175657.png" data-ngthumb="/veranator/nr_000_20250119_175657.png"></a>
    <a href="/veranator/nr_000_20250119_175744.png" data-ngthumb="/veranator/nr_000_20250119_175744.png"></a>
    <a href="/veranator/nr_000_20250119_175815.png" data-ngthumb="/veranator/nr_000_20250119_175815.png"></a>
    <a href="/veranator/nr_000_20250119_175847.png" data-ngthumb="/veranator/nr_000_20250119_175847.png"></a>
    <a href="/veranator/nr_000_20250119_175928.png" data-ngthumb="/veranator/nr_000_20250119_175928.png"></a>
    <a href="/veranator/nr_000_20250119_175955.png" data-ngthumb="/veranator/nr_000_20250119_175955.png"></a>
    <a href="/veranator/nr_000_20250119_181119.png" data-ngthumb="/veranator/nr_000_20250119_181119.png"></a>
    <a href="/veranator/nr_000_20250119_181415.png" data-ngthumb="/veranator/nr_000_20250119_181415.png"></a>
    <a href="/veranator/nr_000_20250119_181508.png" data-ngthumb="/veranator/nr_000_20250119_181508.png"></a>
    <a href="/veranator/nr_000_20250119_182049.png" data-ngthumb="/veranator/nr_000_20250119_182049.png"></a>
    <a href="/veranator/nr_000_20250119_182237.png" data-ngthumb="/veranator/nr_000_20250119_182237.png"></a>
    <a href="/veranator/nr_000_20250119_182427.png" data-ngthumb="/veranator/nr_000_20250119_182427.png"></a>
    <a href="/veranator/nr_000_20250119_182549.png" data-ngthumb="/veranator/nr_000_20250119_182549.png"></a>
    <a href="/veranator/nr_000_20250125_183152.png" data-ngthumb="/veranator/nr_000_20250125_183152.png"></a>
    <a href="/veranator/nr_000_20250125_183946.png" data-ngthumb="/veranator/nr_000_20250125_183946.png"></a>
    <a href="/veranator/nr_000_20250125_185349.png" data-ngthumb="/veranator/nr_000_20250125_185349.png"></a>
    <a href="/veranator/nr_000_20250125_185804.png" data-ngthumb="/veranator/nr_000_20250125_185804.png"></a>
    <a href="/veranator/nr_000_20250125_190145.png" data-ngthumb="/veranator/nr_000_20250125_190145.png"></a>
    <a href="/veranator/nr_000_20250125_190722.png" data-ngthumb="/veranator/nr_000_20250125_190722.png"></a>
    <a href="/veranator/nr_000_20250125_191055.png" data-ngthumb="/veranator/nr_000_20250125_191055.png"></a>
    <a href="/veranator/nr_000_20250125_190722.png" data-ngthumb="/veranator/nr_000_20250125_190722.png"></a>
    <a href="/veranator/nr_000_20250125_191055.png" data-ngthumb="/veranator/nr_000_20250125_191055.png"></a>
    <a href="/veranator/nr_000_20250125_191315.png" data-ngthumb="/veranator/nr_000_20250125_191315.png"></a>
    <a href="/veranator/nr_000_20250125_191530.png" data-ngthumb="/veranator/nr_000_20250125_191530.png"></a>
    <a href="/veranator/nr_000_20250125_191636.png" data-ngthumb="/veranator/nr_000_20250125_191636.png"></a>
    <a href="/veranator/nr_000_20250125_191724.png" data-ngthumb="/veranator/nr_000_20250125_191724.png"></a>
    <a href="/veranator/nr_000_20250125_192023.png" data-ngthumb="/veranator/nr_000_20250125_192023.png"></a>
    
</div>

