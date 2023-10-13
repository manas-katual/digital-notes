---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-3-user-management/021-3-5-1-advance-user-management-2/"}
---

Links : [[Linux Notes/021 RHCSA/021 RHCSA Index\|021 RHCSA Index]]

# Advance user management 2

**Default values that useradd command use while creating a user are stored in 2 files**

<u>/etc/default/useradd</u>
home = /home
shell = /bin/bash
inactive = -1

<u>/etc/login.defs</u>
min uid 1000
max uid 60000


min gid 1000
max gid 60000


min age 0
max age 99999
warn age 7


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

$<div class="markdown-embed-title">

# 500

</div>



==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
shell 
login 
no login 
sh 
bash 
zsh 
/sbin/nologin 
/bin/false 


</div></div>
