A simple backup script written for my personal use.
Script rsyncs current Linux OS to a different device. Device can be USB or internal. /dev/sdx or /dev/nvme1nx
Written and tested using Mint 20.3 Mate only but probably works with most Linux distros, at least as long as
drives are identified by UUID and not just something like /dev/sdx.
As written, it only works with two partitions. A FAT32 EFI boot partition and a single EXT4 main partition.
When run, script asks for the device to clone to, formats it if requested, syncs new/changed files to target device.
And changes UUIDs from old device to the new device so it boots properly.
If a format is requested, files in EFI are also synced; if not formatting, EFI files are assumed working and skipped.

This is very much just a script I cobbled together to suit my personal need and may not suit your needs.
Feel free to use/change it as you wish. Use at your own risk. You can blow away important data, especially if
you choose the wrong device.
I'm not a programmer, just an amateur. Code was written to perform the task I wanted it to do and works for me
but it might not work for you. 
I'm certain the code is not the most efficient or elegant.

What do "I" use it for? I clone my main Linux OS drive to a second drive. A "slave" drive that I can clone back from 
if I mess up the "master". 
Also, to test upgrades, new packages, etc. Boot the slave and do the tests there.
I also clone to a USB Flash drive so I have another backup.
