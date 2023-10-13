---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-3-user-management/021-3-6-7-special-permission/"}
---

Links : [[Linux Notes/021 RHCSA/021 RHCSA Index\|021 RHCSA Index]]

# Special permission

&rarr; Basic permissions :
  - read
  - write
  - execute
==diagram==

&rarr; Special permissions :
  - setUID - SUID - 4
  - setGID - SGID - 2
  - stickybit - 1
==diagram==

&rarr; Stickybit :
  - special permssion
  - Applicable on directories only
  - Restricts delete operation on directories with permission level 777
  - Only owner can delete data

<hr>

Apply stickybit with number
`# chmod 1777 /data55`

Apply stickybit with alphabet
`# chmod +t /data55`

Remove stickybit with alphabet
`# chmod -t /data55`