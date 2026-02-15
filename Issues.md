
### Bluetooth

My bluetooth speaker (JBL Go) was not connecting to my pc

Im not sure why that was, yet I managed to get it working with `bluetoothctl`

The interface is pretty straight forward:

	bluethoothctl
	scan on
	remove *MAC address*
	trust *MAC address*
	pair *MAC address*

Boom -> connected

Now from here I have access to all the actions taken in that same device, volume up, down etc

Now, we were connected but the quality of the audio was terrible.

Audio settings did not show `High Fiddelity Playback ...`

After some search I had to update the `/etc/bluetooth/main.conf` file with *sudo*, yet, this file did not exist

For this I had to install `blueman`

	sudo apt install blueman

Boom the file was present and I had access to the `main.conf`, buuuuut my audio was not coming through the JBL, although sound settings showed it was

I realized it was a problem with Brave, which Im still working on, still in Firefox is working fine

	Note: Brave issue was solved with an update, version: Brave Browser 140.1.82.172 (yes, it does look like an IPv4) 

### Mounting Devices

	uname -srm

When the command runs the terminal displays the kernel version

	lsblk | grep -iE 'sd[a-z]+'

The command displays the list of partitions available on your Linux system.

`-iE
`-i, --ignore-case -> ignore case distinctions in patterns and data
`-E, --extended-regexp -> PATTERNS are extended regular expressions

	sudo mkdir /media/sd-card

Here we create a directory for our *SD* card

	sudo mount /dev/sdb1 /media/sd-card -v

We then *mount* our media

	lsblk | grep -iE 'sd[a-z]+'

And confirm it is mounted

	sudo umount /media/sd-card -v

Unmounting