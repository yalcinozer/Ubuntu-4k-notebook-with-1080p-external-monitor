# Ubuntu 4k notebook with a 1080p external monitor
A simple terminal command to configure multiple monitors for Ubuntu.


#### Why did I created a repo for such a simple and specific topic?

I spent more than 10 hours in total to get the result I wanted. I have tried many recommended codes on the internet but they did not work. Since I was finally bored, I set my 4k monitor to 1080p rather than bothering me with this situation. I used it for 2-3 weeks as this way. It was blury as hell.

Then I start trying all code combinations I found on internet. I reached the desired result with the code I shared here. This setting assumes that you have positioned your monitor above the notebook screen.


xrandr --output HDMI-1-1 --mode 1920x1080 --scale 2x2 --pos 0x0 --rotate normal --output eDP-1-1 --primary --mode 3840x2160 --pos 0x2160 --rotate normal


- You probably will need to replace outputs (HDMI-1-1 and eDP-1-1) with yours.
- You can customize resolutions and positions for your needs
