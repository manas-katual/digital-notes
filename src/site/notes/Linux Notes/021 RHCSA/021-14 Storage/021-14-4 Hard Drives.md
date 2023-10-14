---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-14-storage/021-14-4-hard-drives/","noteIcon":"","created":"2023-10-08T14:04:08.903+05:30","updated":"2023-10-13T17:11:09.326+05:30"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Hard Drives

- **Partition table** : It is the index table that contains entries of all the partitions that exists on a hard drive. There are 2 types of partition table :
	- **MBR (MSDOS) style** :
		- It is a 64-bytes partition table stored inside the MBR
		- This partition table can have entries of up to **4 partitions** only
		- Hence, in this type of partition table, partitions are of 2 types
			- **Primary** : Can be used directly
			- **Extended** : Cannot be used directly. This partition can be further divided into logical volumes. There can be up to 64 logical volumes.
		- A single partition can be scaled up to 2TB
	- **GPT style** :
		- This type of partition table can have entries of up to **128 partitions**
		- There are no partition types
		- All partitions can be used directly
		- Partitions are known by the name tags
		- Partition size can go beyond 2TB