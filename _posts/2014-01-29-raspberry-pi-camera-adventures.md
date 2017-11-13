---
title: Raspberry Pi Camera Adventures
author: Ryan McDermott
layout: post
permalink: /raspberry-pi-camera-adventures/
categories:
  - Uncategorized
---
This weekend I had an amazing time with the Raspberry Pi camera &#8212; I know, it sounds like I am describing a first date! I was surprised by how easy it was to install. I was considering a blog post here to show you how to install it but far and away the best explanation video I&#8217;ve seen out there is from the Raspberry Pi makers:[ http://www.raspberrypi.org/camera][1]

This is what my future little Hal looked like when it was all set up:

<div id="attachment_190" style="width: 778px" class="wp-caption alignnone">
  <a href="http://ryansworks.com/wp-content/uploads/2014/01/IMG_2922.jpg"><img class="size-large wp-image-190" alt="IMG_2922" src="http://ryansworks.com/wp-content/uploads/2014/01/IMG_2922-768x1024.jpg" width="768" height="1024" /></a>
  
  <p class="wp-caption-text">
    Total Install time: 30 seconds
  </p>
</div>

Then the really neat part was turning it on, I didn&#8217;t think it would light up or anything:

[<img class="alignnone size-large wp-image-192" alt="IMG_2924" src="http://ryansworks.com/wp-content/uploads/2014/01/IMG_2924-768x1024.jpg" width="768" height="1024" />][2]

And finally, I got my first picture taken with the camera:

[<img class="alignnone size-large wp-image-195" alt="IMG_2925" src="http://ryansworks.com/wp-content/uploads/2014/01/IMG_29251-768x1024.jpg" width="768" height="1024" />][3]

Next on my agenda is to get the FIFO buffers working and to stream the video with a reasonable amount of speed. Theoretically it is possible to have this stream in real-time. The question I have going forward is how far can we push the Pi? I don&#8217;t mean off the table! What are the real processing limits. If we attach servos, Arduinos, and gizmos through the GPIO port, will the camera&#8217;s streaming take a major hit! That&#8217;s what I&#8217;ll be finding out going forward.

 [1]: http://www.raspberrypi.org/camera
 [2]: http://ryansworks.com/wp-content/uploads/2014/01/IMG_2924.jpg
 [3]: http://ryansworks.com/wp-content/uploads/2014/01/IMG_29251.jpg