---
layout: post
date: 2018-01-31 10:00
title: "Interesting - Elphel 4 camera mid range stereo"
author: jim
category:

tags:
- home1

---

![Elphel](https://blog.elphel.com/wp-content/uploads/2017/09/MNC393-XCAM.jpeg)

 Elphel have a <a href="https://blog.elphel.com/2017/09/long-range-multi-view-stereo-camera-with-4-sensors/"> very interesting piece</a> on a 4-camera approach to real-time mid-range RGBD. The core of the approach is to use block matching, and to target sub-pixel accuracy and to avid intermediate representations. To see a demo of their results  <a href="https://community.elphel.com/3d+map/?lat=44.71551373&lng=-116.89453125&zoom=5&rating=5"> try their scene viewer</a> . Click on a picture on the left, then a numbered link under the thumbnail and play around with the RGBD image.

I think this is potentially a great platform for mid-range (5-200m) depth mapping in the optical domain, which can then be used in a variety of methods. A simple one would be to provide labelled data to support occlusions in people tracking, but I think there's a lot more here.

 [Image above from <a href="https://www.elphel.com"> elphel</a>] 










