---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-14-storage/021-14-7-swap-management/","noteIcon":"","created":"2023-10-11T14:36:30.324+05:30","updated":"2023-10-14T23:16:50.448+05:30"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Swap management

- Swapping is a memory management technique used in multi-programming to increase the number of processes sharing the CPU.
- It is a technique of removing a process from the main memory and storing it into secondary memory, and then bringing it back into the main memory for continued execution
- This action of moving a process out from main memory to secondary memory is called Swap Out and the action of moving a process out from secondary memory to main memory is called Swap In
- A default swap partition is created while Linux installation
- The size of the the default swap partition is double the size of RAM
- However, if the default partition is full of swapped out processes, then we can increase overall swap by creating additional swap partition
- The new partition gets higher priority so that new swapped out processes get stored on the new partition