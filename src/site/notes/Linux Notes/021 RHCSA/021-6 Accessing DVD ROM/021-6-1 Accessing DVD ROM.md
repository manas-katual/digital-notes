---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-6-accessing-dvd-rom/021-6-1-accessing-dvd-rom/","noteIcon":"","created":"2023-10-07T13:47:51.574+05:30","updated":"2023-10-13T17:08:57.266+05:30"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Accessing DVD ROM

**Steps to access a DVD Rom in Linux**

1. Connect DVD to a VM
	![DVD.png](/img/user/Linux%20Notes/assets/DVD.png)
	![DVD 2.png](/img/user/Linux%20Notes/assets/DVD%202.png)
1. Detect DVD Rom in Linux
	<abbr title="dmesg shows all hardware information">`# dmesg | grep sr0`</abbr>
3. Mount DVD ROM on Mount point
	`# ls /mnt`
	`# mount /dev/sr0 /mnt`
4. Access data via mount point
	`# ls /mnt`
5. Unmount DVD Rom from mount point
	`# unmount /mnt`
	`# ls /mnt`

<hr>

>[!info]
**Device driver for DVD Rom is /dev/sr0
/mnt is by default available in Linux for mounting DVD Rom or USB drive
Installation DVD of RHEL 8 contains setup of 7000+ opensource software**

