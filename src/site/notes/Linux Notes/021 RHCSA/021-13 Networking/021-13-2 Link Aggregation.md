---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-13-networking/021-13-2-link-aggregation/"}
---

Links : [[Linux Notes/021 RHCSA/021 RHCSA Index\|021 RHCSA Index]]

# Link Aggregation

- Ethernet cards come with fixed bandwidth **(I0mbps, 100mbps,1gbps, 10gbps 100gbps)**
- If bandwidth of a single network card on a server is insufficient to handle network payload, then we can add more network cards on the server and logically group them io increase throughput
- This mechanism is called **link aggregation**
- In link aggregation, a logical network interface called **bond interface** is created
- **Bond** interface becomes the **master** and the **physical cards** (eth0, eth1) become **slave of bond**
- IP address is configured on bond and not on physical cards
- MAC address still stay on physical cards
- All the network traffic will be load balanced between slave cards by bond interface, thus provide **high throughput**
- 
- **LACP** protocol is used
- A single bond interface can have up to 16 network cards