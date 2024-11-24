A simple backup script written for my personal use.
It rsyncs current booted Linux OS to a different device. Device can be USB or internal. /dev/sdx or /dev/nvmexnx
Written and tested using Mint 20.3 Mate but may work with other Linux distros, at least as long as
drives are identified in /etc/fstab by UUID.
It only works with two partitions because that's all I needed. A FAT32 EFI boot partition and a single EXT4 main partition.
When run, script asks for the device to clone to, formats it if requested, and syncs new/changed files to the target.
It also changes UUIDs from those of the old device to those of the new device so it boots.

This is just a script I cobbled together to suit my personal need but it may not suit your needs.
Feel free to use/change it as you wish. Use at your own risk. You can lose important data, especially if
you choose the wrong device as the target.
I'm not a programmer, just a do-it-yourselfer. Code was written to perform the task I wanted it to do and it works for me. It may or may not work for you.
I'm sure the code is not the most efficient or elegant.

What do "I" use it for? I clone my main Linux OS drive to a second device. A slave/portable/backup drive that I can clone back from if I mess up the "master".

Also, to test new configs, new packages, etc. I boot to the slave and do the tests there.
I also clone to a USB Flash drive so I have another backup.
