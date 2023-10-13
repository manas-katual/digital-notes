---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-3-user-management/021-3-5-advance-user-management/"}
---

Links : [[Linux Notes/021 RHCSA/021 RHCSA Index\|021 RHCSA Index]]

# Advance User Management


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

$<div class="markdown-embed-title">

# 300

</div>



==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
useradd ganesh 
User
Group 
UID
GID 
Home directory
Profile files (default) 
primary 
unique 


</div></div>


- When a user is created its group also get created and his association will be primary
- And also its UID & GID get created 
- UID stands for User ID
- GID stands for Group ID
- Every users UID is unique & Every Groups GID is unique
- Minimum UID & GID value for local users and group is 100 it is incremental by 1
- UID and GID '0' is always assigned to root and its group
- 1-999 is reserved for system users & groups.
- Default maximum limit for UID and GID is 60000. But it is changeable it can be increased or decreased.
- Every user is given profile files. Profiles are loaded every time when a user will login. Profile files are always hidden and are stored in user's home directory. It is called ".bashrc"



<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

$<div class="markdown-embed-title">

# 800

</div>



==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
Profile file types 
Personal 
Common 
- Present in the home
  directory of every user
- File name is .bashrc
- Personal for every user 
- A common profile
  file for all users
- File name is
  /etc/bashrc
- Only root can modify this file 
User login 
.bashrc 
/etc/bashrc 


</div></div>
