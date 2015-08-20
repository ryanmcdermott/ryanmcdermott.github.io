---
title: Towards a Triggering Language
author: Ryan McDermott
layout: post
permalink: /towards-a-triggering-language/
dsq_thread_id:
  - 
categories:
  - Uncategorized
---
Let us fast forward 50 years. We are living in a world of connected devices. Everything around us responds intelligently to our needs, wants, and emotions. We awake on a weekend morning:

The lights turn on slowly as your bed detects you slowly rising after your sleep. Your coffee pot fills with water and heats itself to a simmer.  You saunter over into your kitchen. Your fridge recommends foods based on readings from your latest medical checkup. As you begin to eat, music comes on mezzo forte through your stereo. It best matches your current mood based on natural language processing of yesterday&#8217;s text messages. You walk into your living room and look for your keys. They ring to alert you where they are, knowing already that you have a scheduled Frisbee meetup at the local park. Your car turns itself on as you walk outside. As you get in, it begins to drive itself. You read the latest news on your phone and as you get to a stop light, there&#8217;s an explosion of in the distance. You look on, with a confounded expression. Emergency personnel are alerted to the area based on decibel readers installed on all public land in your municipality. Must have been a gas line break, you assume. You make it to the Frisbee field and your car knows exactly the optimal place to park. You step outside, and enjoy the day, unaware of the bytes whirling around you that are as much a part of your day as the people and things you love.

Let&#8217;s go back in time now, to the present moment. When we look at this future world, one thing is clear: there&#8217;s truly intelligence to our &#8220;smart&#8221; devices. Devices seem to be communicating with one another. How though? How is it that the lights know when to turn on? How does the coffee pot know to start? How is it that anything knows what to do, for, to, and with another device or set of devices? We can certainly reduce this down to something very simple: a series of &#8220;if this, then that&#8221; cases.

This is an attractive thought. After all, we can think of this, along with many other complex phenomena in life, as simply input and output, or cause and effect. If [morning], then [lights\_on]. If [woken\_up], then [coffee_starts]. This simplistic way of looking at the problem. Is this something though that we can actually use technically? Is our world really going to be a series of if and then statements, or will we live with a richer set of conditionals?

I would bet my bucks on the latter. The world is messy. Why wouldn&#8217;t our devices conform to that? Decibel readers in a city wouldn&#8217;t simply trigger emergency teams if they detect a higher decibel level than the set threshold. Proximity to crime, density of population in the area, and history of explosions are all things that would be factored in. Not to mention, all other relevant data.

Simple if then, and even else, cases don&#8217;t work well enough to capture these kinds of conditionals in the real world. What we need is a triggering language for M2M communication. One that can handle loops, comparisons, routing data to other devices, sending actions, executing system calls, negation, and normal if, elseif, else cases. A primitive example of such a language could look something like this:

    if ([dev] [reports] X or [system call returns] Y){
    	to device, device, device do action with [data];
    }
    
    unless ([dev] [reports] Y) {
    	to device do action;
    }
    
    

This is a very basic example alone but it handles a much wider array of cases. Let&#8217;s look at what such a clause of this language would look like with a real world example:

    if ([moisture_detector] [report] == "water" or [syscall: time_to_end] == true){
    	to sprinkler1, sprinkler2, sprinkler3 do [turn_off] with [data: slow];
    }
    
    unless ([moisture_detector] [reports] "water") {
    	to sprinkler1, sprinkler2, sprinkler3 do [water_grass];
    }
    
    

There are many advantages to this approach. You can do analysis with data returned from the device and compare it to report codes. Furthermore, you can specify loops of actions, as well as multiple routes for data. Another advantage is that being able to call system functions and act on their returned data, whether the function is on the device or a server, allows you more intelligent processing, reporting, and actuating on any device. Simple if then cases won&#8217;t suffice with large sensor and actuator systems. Imagine the spaghetti code of conditionals! These communication fragments are the currency of future AI systems for these sensor networks. Conditionals and triggers change as AI dictates. Imagine what the AI system would do when it finds out your water bill is too high! That *unless* case would include an *and* clause that makes a comparison with your budget. There&#8217;s an infinite amount of things that are possible with this kind of approach, and I think it&#8217;s one worth exploring.

Stay tuned for further blog posts as I continue on this endeavor, one I call **MTL: Machine Triggering Language**