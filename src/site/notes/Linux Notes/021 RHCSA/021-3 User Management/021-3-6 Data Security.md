---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-3-user-management/021-3-6-data-security/","noteIcon":"","created":"2023-10-07T13:47:51.476+05:30","updated":"2023-10-13T17:07:54.425+05:30"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Data Security

- All the data on a server is in the form of files and directories
- A file is an end object
- A directory is a container
- On a single server there can be multiple user accounts
- There can be a lot of data on a server belonging to various users and groups
- In order to control access of data for users and groups we must define data security
- File and directory permissions are set to achieve data security
- Since file and directory are 2 different type of objects, the concept of permission is bit different for both

For e.g.
- Every website is a collection of files and folders
- If a hacker tries to hack your website by downloading index.html or any file and change its content and upload it back to the website (server) it will be huge loss to the company
- In order to prevent it from happening we have to give files permission to read only to the user so that any hacker would not be able to modify it