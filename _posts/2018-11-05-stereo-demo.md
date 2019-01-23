---
layout: post
date: 2018-11-05 10:00
title: "Mid range stereo early demo"
author: jim
category:

tags:
- home1

---

![Stereo Depth]({{ site.url}}/assets/content_img/im160.jpg)

I have spent a lot of the year looking at depth from stereo, or photogrammetry. Inspired by <a href="https://www.elphel.com"> Elphel</a> who are using high-res commodity CMOS sensors for mid/long range depth from stereo, I've taken a slightly different angle. Instead of using DCT matching to get sub-pixel resolution, I've been experimenting with direct block matching at the Bayer CFA pattern level. It's not yet clear whether this is a fundamentally better or worse approach than using the Fourier domain, but I have some early results.

The current set up is from taking still images from a Ricoh GR (prime lens, no low-pass filter) and then matching them. Baseline is usually 25cm. I can currently get approximately 1/4 subpixel matching off tiled 16 pixel blocks. Z accuracy is roughly 1% at 50m, 2% at 100m.

Still early days but I've started to get some results.
An example is below. Next steps include separating out 2 surfaces when they overlap on one block, then looking at possible hardware platforms, performance, use cases and people to work with.

#### Sample Stereo depth video - Work in Progress

<iframe width="1280" height="720" src="https://www.youtube-nocookie.com/embed/Nvkck41eLhk?rel=0" frameborder="0" allowfullscreen></iframe>

In the video above, the animated grey masks blocks  beyond a certain z distance to the camera. The animation shows z distance  decrease then increase at 1/4 subpixel matching steps. It shows 8 pixel square blocks in x,y direction. The image is 2k x 1k cropped  from larger 12MP image.

Unmatched pixels show occlusions which appear to the left of foreground objects, and errors due to mis-match, other errors include specular reflection (car) ,low-light (under the car) and uniform horizontal features on the house.


This video shows the data from one frame displaying 2k x 1k, A key question is whether it is possible  to deliver multiple frames per second , using full 5MP/ 8MP camera or similar. Please email me jimd -at- yantantethera.com if you have any questions.
