---
title: Raspberry Pi In the Sky
author: Ryan McDermott
layout: post
permalink: /raspberry-pi-in-the-sky/
categories:
  - Uncategorized
---
So begins my journey. One I set out to accomplish as a sort of New Year&#8217;s Resolution (along with more sustained blogging) I&#8217;ve begun my odyssey into the world of the Raspberry Pi.

<div id="attachment_146" style="width: 235px" class="wp-caption alignnone">
  <a href="http://ryansworks.com/wp-content/uploads/2014/01/IMG_2895.jpg"><img class="size-medium wp-image-146" alt="Setting up the Pi for the first time." src="http://ryansworks.com/wp-content/uploads/2014/01/IMG_2895-225x300.jpg" width="225" height="300" /></a>
  
  <p class="wp-caption-text">
    Setting up the Pi for the first time.
  </p>
</div>

<span style="line-height: 1.5em;">Yes Milton, that&#8217;s a stapler holding the wires down. That thumbnail image is damn-near the size of the actual Pi. It could fit into your wallet if you were so audacious, and if you wanted to plug your wallet into the Internet of Things ® (more on that to come) Excuse the Amazon endorsement, but I got the complete <a href="http://www.amazon.com/CanaKit-Raspberry-Complete-Original-Preloaded/dp/B008XVAVAW">CanaKit setup</a>, partially out of laziness because I didn&#8217;t want to buy an HDMI cable, SD card, and power supply all separately. I unfortunately didn&#8217;t have any lying around.</span>

The setup they give you comes with a flashed SD card with NOOBS installed, which acts as a bootloader to help you configure your distro of Linux. The Raspbian one looks rather swell, so no problems there. If you want to flash any old SD card just run dd on the device name. You can find a good install guide here which I ran with a friend on a separate install: [http://elinux.org/RPi\_Easy\_SD\_Card\_Setup][1]

<div id="attachment_151" style="width: 310px" class="wp-caption alignnone">
  <a href="http://ryansworks.com/wp-content/uploads/2014/01/IMG_2896.jpg"><img class="size-medium wp-image-151" alt="A great first date with the Pi" src="http://ryansworks.com/wp-content/uploads/2014/01/IMG_2896-300x225.jpg" width="300" height="225" /></a>
  
  <p class="wp-caption-text">
    A great first date with the Pi
  </p>
</div>

My first task was to set up an SSH server on there. The beauty is that you don&#8217;t need that old monitor any more. Just SSH into the Pi on your local network and run apt-get all day and have fun. I ordered a camera along with it and I am installing that now after writing this cheeky blog post. I&#8217;m installing OpenCV on the Pi as well (warning it takes a while) and using some of the library to run motion detection from still images captured by the Pi. Wish me luck!

 [1]: http://elinux.org/RPi_Easy_SD_Card_Setup