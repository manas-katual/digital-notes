---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-3-user-management/021-3-2-basic-user-management-commands/","noteIcon":"","created":"2023-10-07T13:47:51.413+05:30","updated":"2023-10-13T17:07:07.680+05:30"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Commands

1. `# useradd jane` &rarr; Add a user account
2. `# usermod -l jake jane` &rarr; Change a username
3. `# passwd jane` &rarr; Set/Change password for a user
4. `# passwd -d jane` &rarr; Remove password for a user
5. `# passwd -l harry` &rarr; Lock a user Account
6. `# passwd -u harry` &rarr; Unlock a user Account
7. `# su - jane` &rarr; switch user on same terminal with home directory
8. `# chfn harry` &rarr; Add finger (personal) info
9. `# finger harry` &rarr; view finger info 
10. `# userdel harrry` &rarr; Delete a user (without deleting home directory)
11. `# userdel -r harry` &rarr; Delete a user (with home directory)
12. `# getent passwd jane` &rarr; Get info of a user account
13. `# getent passwd` &rarr; List all existing users