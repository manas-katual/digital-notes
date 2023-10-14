---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-2-f-ile-management/021-2-4-search-commands-on-linux/"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Search Commands

To search any file or folder on Linux commands are as follows

## Find
- find command is used to search data in bulk
- various criteria to search data
- name pattern, file size, type, creator
- no database file
- search data in real directory structure
- we need to provide a target directory

## locate 
- By using this command we can locate any file or folder absolute path
- It's database is inside `/var/lib/mlocate/mlocate.db`
## updatedb  
- It is best practice to update the database of file system before using locate command
## pipline | 
- 2 or more commands to derive a single output It is represented as "|". ==(example comming soon) ==