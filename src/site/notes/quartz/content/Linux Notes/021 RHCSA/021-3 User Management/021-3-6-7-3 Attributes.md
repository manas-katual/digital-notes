---
{"dg-publish":true,"permalink":"/quartz/content/linux-notes/021-rhcsa/021-3-user-management/021-3-6-7-3-attributes/","noteIcon":"","created":"2023-10-14T22:10:59.634+05:30","updated":"2023-10-13T17:08:33.980+05:30"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Attributes

- Permissions restrict local users from accessing files and directories 
- root always has full access of files and directories
- In order to restrict root from accessing files and directories, we can configure attributes
- Attributes are meta-data properties that describe a file or directory's behaviour
- There are plenty of attributes for files and directories
- Few commonly used attributes are :
	- **a** - it means a file can only be appended with new data. Existing data cannot be modified or removed
	- **A** - it means modify time of the file or directory will not update
	- **i** - it means a file or a directory is immutable
- `chattr` command is used to set/unset an attribute
- `lsattr` command is used to list current attributes of a file or a directory

==Attributes restrict access for root as well==