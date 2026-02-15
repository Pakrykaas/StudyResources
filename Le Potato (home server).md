
**OBS: All the action depicted here under take place from an original Ubuntu environment

Once I got my Le Potato s905x I decided to take it for a ride (with a great knowledge gap)

I started out by checking some youtube video, were an *armbian* distro was used.

The process was simple, flashing the microSD with the distro we want, insert it and plug the potato to a router

From there we should access the router's home page and from there we would get an IP to which we would connect via SSH

So of course, I went ahead and did exactly this, till after 2 days I realized that the best kept distro is the *raspbian*

The first distro I tried was *debian*, the issues I was facing went from not being able to connect via SSH `connection refused` to not having any output to a monitor.

I checked my router's firewall and all seemed cool, until I found out that only *armbian* was ready to have a root user created in the first SSH login

I changed to *raspbian* but had a bit of a hard time with `dd`, finding out soon after that the causes to my issue resided in the fact that I should be using `rpi-imager` a GUI tool that allows us to flash memories in a pretty straight forward and effective way

The syntax is pretty straight forward:

	sudo apt install rpi-imager
	rpi-imager <image.img>

The GUI pops up, from there you choose the image and the drive you want to flash

The process is fairly fast

Once I connected Le Potato to a screen and keyboard I was able to login (full CLI environment), went ahead and updated the `/etc/systemd/network` in order to connect the WiFi but somehow I was not able to run updates

I followed the steps in https://hub.libre.computer/t/debian-12-bookworm-and-11-bullseye-for-libre-computer-boards/230 ![[Pasted image 20251026003129.png]] But still I was unable to update my distro, thats when I moved to *raspbian

This distro is just any regular GUI based distro, from install to use, still, I was having latency issues.

All was going good till the moment my Potato froze and I had to restart it (most likely I need to increase the *swap* space, no big deal) and I was prompted to a full CLI environment

Will work on this again tomorrow

### 
