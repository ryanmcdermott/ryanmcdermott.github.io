---
title: 'Start Your Engines &#8211; Nginx'
author: Ryan McDermott
layout: post
permalink: /raspberry-pi-nginx/
categories:
  - Uncategorized
---
On something the size of a credit card you can run what would have been one of the world&#8217;s most powerful web servers from the 90s. That idea alone is fascinating enough to get a server going on my Pi, but more than that, having that little gizmo serve up data opens so many possibilities. Imagine being able to put one of these in your house or apartment and have a webserver running on it than can give you access to the CPU info, and control attachments like a camera, alarm, or wheels. There&#8217;s so much this little guy can do, so I thought why not dive in and set up Nginx.

It&#8217;s trivially simple to get going. First things first &#8212;  I wanted to configure my Wifi dongle to connect to my local network. I didn&#8217;t want to have my Pi sitting on top of my router with an ugly Ethernet cable plugged into it. That feels very *unRaspberry. *Initially though, I had to connect my Pi to my local network. When you do this, login to your router and grab the local connected hosts and find the hostname of your Pi as I did and get the associated IP address.

<div id="attachment_173" style="width: 310px" class="wp-caption alignnone">
  <img class="size-medium wp-image-173" alt="You can also use nMap to find connected clients ;)" src="http://ryansworks.com/wp-content/uploads/2014/01/Screen-Shot-2014-01-21-at-11.21.07-PM-300x24.png" width="300" height="24" />
  
  <p class="wp-caption-text">
    You can also use nMap to find connected clients ;)
  </p>
</div>

SSH into your Razzy:

`ssh [IP_ADDRES] -l pi`

Enter the password you set up when you configured your Pi for the first time.

From here on out it&#8217;s not at all complicated. This is optional but I installed vim, my favorite text editor. After that I sudo opened /etc/wpa\_supplicant/wpa\_supplicant.conf

`sudo vim /etc/wpa_supplicant/wpa_supplicant.conf`

Where it says ssid enter the name of your Wifi router (for all Python nerds, I called mine AwesomeVanRossum) Where it says psk, enter your password. Subsequent to that, I rebooted my Pi and it came up perfectly with Internet access! Verify that by logging into your router and see if you can see a connected client with your Pi&#8217;s hostname.

Now all I did was I typed *sudo apt-get install nginx *into my SSH session:

<img class="alignnone size-medium wp-image-174" alt="InstallNginx" src="http://ryansworks.com/wp-content/uploads/2014/01/Screen-Shot-2014-01-22-at-10.54.23-PM-300x134.png" width="300" height="134" />

Nginx normally listens on port 80. Now as a mild amount of security through, but not solely, obscurity I changed the port that Nginx listens on. I set it to 8080 instead. Easy to remember and not occupied by any major protocol other than proxies and such. You&#8217;re still vulnerable to a port scan and the like, but I don&#8217;t worry to much about it. Don&#8217;t keep secure data on your Pi and turn it off when you want to use your network securely. Anyway, to change the listening port for Nginx I typed:

`sudo vim /etc/nginx/sites-enabled/default`  
I then uncommented the line that said #listen. I set it to *listen 8080*

After that it&#8217;s easy, I just typed in `sudo service nginx start`

You&#8217;ll need to login to your router and set it to port forward to your Raspberry Pi. Like so:

<img class="alignnone size-medium wp-image-176" alt="Port Forward" src="http://ryansworks.com/wp-content/uploads/2014/01/Screen-Shot-2014-01-22-at-12.08.39-AM-300x36.png" width="300" height="36" />

Now when you navigate to your router&#8217;s external IP address, which you can find at <www.whatismyip.com>, (i.e. 25.15.32.10:8080) You should see this:

<img class="alignnone size-medium wp-image-177" alt="You're Online" src="http://ryansworks.com/wp-content/uploads/2014/01/Screen-Shot-2014-01-21-at-11.34.54-PM-300x84.png" width="300" height="84" />