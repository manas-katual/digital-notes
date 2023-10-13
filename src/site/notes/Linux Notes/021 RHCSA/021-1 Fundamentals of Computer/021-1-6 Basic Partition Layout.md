---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-1-fundamentals-of-computer/021-1-6-basic-partition-layout/"}
---

Link : [[Linux Notes/021 RHCSA/021 RHCSA Index\|021 RHCSA Index]]

# Partition Layout

There are two types of partition layout

## Single Partition Layout

- Entire Filesystem is created on a single partition.
- Drawback is that if the partition is corrupted, then all system and user data is lost.
- Suitable for R&D servers

## Multiple Partition Layout

- **"/"** becomes the main system partition and while we have etc, usr, lib, proc, root, tmp and dev directories on itself
- boot, home and var can be declared as mount points of separate partitions


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

$<div class="markdown-embed-title">

# 800

</div>



==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
Single Partition Layout 
/ 
etc
usr
lib
proc
root
tmp
home
var
dev
boot 
100 GB 
Multiple Partition Layout 
/ 
/var 
/boot 
/home 
etc
usr
lib
proc
root
tmp
dev 
50 GB 
20 GB 
10 GB 
20 GB 


</div></div>


## Swap Partition

- In Linux there is a special partition called swap partition in other words it is virtual memory. It is also known as paging process.
- It provides extra RAM to the system.
- For example if there is 4gb RAM in the system and all the processes are full (RAM is full) then the system (RAM) borrows some space from the storage and it that storage acts as a RAM.
- It is a temporary RAM


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

$<div class="markdown-embed-title">

# 800

</div>



==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
HDD  -  60 GB 
1 GB  /boot 
10 GB  /var 
40 GB  / 
4 GB  /home 
Swap Partition
    4 GB 
4 GB 
RAM 
overload 
Paging Process 
Process 
 6 GB 
Server hang
Server reboot 
HDD 
Process
Swap 
reserved
partition
for RAM 
99.9 % full 
Virtual Memory 
double the size of RAM or atleast
4 GB 


</div></div>



