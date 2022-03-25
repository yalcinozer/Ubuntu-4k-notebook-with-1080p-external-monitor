# Ubuntu 4k notebook with a 1080p external monitor
A simple terminal command to configure multiple monitors for Ubuntu.


#### Why did I create a repo for such a simple and specific topic?

I spent more than 10 hours in total to get the result I wanted. I have tried many recommended codes on the internet but they did not work. Since I was finally bored, I set my 4k monitor to 1080p rather than bothering me with this situation. I used it for 2-3 weeks this way. It was blurry as hell.

Then I start trying all the code combinations I found on the internet. I reached the desired result with the code I shared here. This setting assumes that you have positioned your monitor above the notebook screen.


xrandr --output HDMI-1-1 --mode 1920x1080 --scale 2x2 --pos 0x0 --rotate normal --output eDP-1-1 --primary --mode 3840x2160 --pos 0x2160 --rotate normal

- You probably will need to replace outputs (HDMI-1-1 and eDP-1-1) with yours.
- You can customize resolutions and positions for your needs

Edit

After formatting my disk and installing a fresh Ubuntu 18.04, the code above did not give the result I wanted. After hours of research, the code below gave runs perfectly for me. For some reason "--scale" does not give very stable results. This command prevents the zoom effect and scales the external screen by two, so the sizes of screens matched perfectly. (1080p and 2160p screens)

xrandr --output HDMI-1-1 --mode 1920x1080 --transform 2,0,0,0,2,0,0,0,1
