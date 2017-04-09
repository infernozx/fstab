# /etc/fstab: static file system information.
#
# Use 'blkid' to print the universally unique identifier for a
# device; this may be used with UUID= as a more robust way to name devices
# that works even if disks are added and removed. See fstab(5).
#
# <file system> <mount point>   <type>  <options>       <dump>  <pass>
proc            /proc           proc    nodev,noexec,nosuid 0       0
# / was on /dev/sdb1 during installation
UUID=ef05afeb-1817-498d-9dfb-b2330280db14 /               ext4    errors=remount-ro 0       1
# /home was on /dev/sda1 during installation
UUID=1aee0d13-5684-4402-936e-4f8c8b5b2af1 /home           ext4    defaults        0       2
# swap was on /dev/sda5 during installation
#UUID=068c9c6e-8d75-4f4e-b014-9123b95956b0 none            swap    sw              0       0
/dev/mapper/cryptswap1 none swap sw 0 0
#192.168.1.254:/mnt/HD/HD_a2 /home/tarrant/Serverator nfs auto,noatime,nolock,bg,nfsvers=3,intr,tcp,actimeo=1800 0 0
