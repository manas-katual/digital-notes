---
{"dg-publish":true,"permalink":"/quartz/content/linux-notes/021-rhcsa/021-9-service-management/021-9-3-targets/","noteIcon":"","created":"2023-10-14T22:10:59.678+05:30","updated":"2023-10-13T17:10:00.967+05:30"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Targets

- In Latest Linux kernels running with system, run-levels are enhanced to targets
- Targets are known by names
- The targets available in Linux are :
	- **halt.target** is equivalent to [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^27b2cc\|Run-level 0]] 
	- **rescue.target** is equivalent to [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^af6df5\|Run-level 1]] (recovery console with read/write access)
	- **emergency.target** is equivalent to [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^af6df5\|Run-level 1]] (recovery console with read only access). It is basically given to freshers so that they can't modify anything they can only report the error.
	- **multi-user.target** is equivalent to [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^0ae377\|Run-level 3]] 
	- **graphical.target** is equivalent to [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^1f4167\|Run-level 5]]
	- **reboot.target** is equivalent to [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^c1c2ef\|Run-level 6]]

---

- Out of all the target, any 1 target will be **default target**
- The default target is the target in which the system boots
- The default target should be either multi-user.target or graphical.target

---

>[!Note]
>- **rescue.target** & **emergency.target** both are equivalent to [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^af6df5\|Run-level 1]] so it is not a typo
>- [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^bd8387\|Run-level 2]] and [[quartz/content/Linux Notes/021 RHCSA/021-9 Service Management/021-9-2 Run Levels#^0ae377\|Run-level 4]] are not there in targets. I mean there is no concept of run-level after 3.x Linux version

---

## Commands

- To know current target
`runlevel` &rarr; it may work or maynot because it is outdated

- To switch to a target
`systemctl isolate multi-user.target`

- To know the default target
`systemctl get-default`

- To change default target
`systemctl set-default <target name>`
