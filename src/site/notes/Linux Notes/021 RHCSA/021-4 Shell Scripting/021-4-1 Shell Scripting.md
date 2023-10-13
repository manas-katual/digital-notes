---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-4-shell-scripting/021-4-1-shell-scripting/"}
---

Links : [[Linux Notes/021 RHCSA/021 RHCSA Index\|021 RHCSA Index]]

# Introduction 

- Shell scripting is used to to run a bunch of commands
- If we want to run multiple commands with one single command we can use shell scripting

### Steps to create a script

1. Create a new text file using text editor
2. Write valid Linux commands 
3. Save the file
4. assign execute permission to the file


### Run a script

- By default, we cannot run a script like a command
- we provide absolute path of the script
- we can make a script run as a command by copying or moving it to `/usr/bin` OR `/usr/sbin`