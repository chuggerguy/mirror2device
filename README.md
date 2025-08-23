A simple backup script written for my personal use. (cloning/backing up my Mint Mate installs, it may or may not work with other distros)
It rsyncs current booted Mint OS to a different device. Device can be USB or internal. /dev/sdx or /dev/nvmexnx
Written and tested using Mint Mate but may work with other Linux distros, at least as long as
drives are identified in /etc/fstab by UUID.
It only works with two partitions because I wrote it for me and that's what I needed. A FAT32 EFI boot partition and a single EXT4 main partition.
When run, script asks for the device to clone to, formats it if requested, and syncs new/changed files to the target.
It also changes UUIDs from those of the old device to those of the new device so it boots.

This is just a script I cobbled together to suit my personal need. It may or may not suit your needs.
Use at your own risk. You can lose important data, especially if
you choose the wrong device as the target.
I'm not a programmer, just a do-it-yourselfer. Code was written to perform the task I wanted it to do and it works for me.
I'm sure the code is not the most efficient or elegant. Maybe not "pretty" code, but it works.

What do "I" use it for? I clone my main Mint Mate Linux OS drive to a second device. A slave/portable/backup drive that I can clone back from if I mess up the "master".

Also, to test new configs, new packages, etc. I boot to the slave and do the tests there.
I also clone to a USB Flash drive so I have another backup.

Disclaimer: I realize this does not produce a true drive clone. It's not a bit by bit copy of the drive. Perhaps it should be called an OS clone? Or maybe not. :)
If you decide to try it, I'd suggest you test it on a spare USB flash device. 
This is a boring video of it in action. I had just got a new flash drive so it includes formatting.
https://www.youtube.com/watch?v=_ImoVuOB_MU
https://www.youtube.com/watch?v=nJhGow-jPwg
