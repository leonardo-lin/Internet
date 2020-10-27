計網小考110屆上集
==

[TOC]

#  Test1

### Q1.
+ please use an example why link-state routing alogorithm would cause route oscillation
   >link cost = amount of carried traffic
   
   >![](https://i.imgur.com/47vwQQ8.png)
   
   >
### Q2.
+ please show how poisoned reverse solve the problem of count-to-infinity



>![](https://i.imgur.com/r9UDknt.png)
>![](https://i.imgur.com/fgV3lLN.png)

### Q3.
+ please compare link-state and distance-vector algorithms in terms of message complexity, convergence speed and robustness
  >
  > LS: with n nodes, E links, O(nE) msgs sent
  > DV: exchange between neighbors only
### Q4.
+ please describe the functions of eBGP and iBGP sessions
  >eBGP:　obtain subnet reachability information from neighboring ASes 
  >eBGP:　存在於AS與AS之間
  >iBGP:　propagate reachability information to all ASinternal routers.
  eBGP:　存在於AS內部
  >![](https://i.imgur.com/j5sQi1l.png)


### Q5.
+ please describe how hot potato routing works
  > choose local gateway that has least  cost
  > 選擇最短路徑直接丟出去

# Test2

### Q1.
+ please explain how internet uses intra-AS and inter-AS routing to achieve scalable routing
  
  >intra 在內部
  >inter 在外部
  >intra : admin wants control over how its traffic routed, who routes through its net. 
  >inter : single admin, so no policy decisions needed


### Q2.
+ 不會please describe the concept and benefits of hierarchical OSPF
  > link-state advertisements only in area 
  >each nodes has detailed area topology; only know direction (shortest path) to nets in other areas.
  >area border router(ARB):連結兩個或以上area的router
  >backbond router:存在於backbond area 的router

  >conecpt: 將OSPF分層
  >benefit: security,multiple(same cost path is allow)
### Q3.
+ 不知道怎麼寫please describe the generation of forwarding-table entries in a router with BGP and OSPF
  >![](https://i.imgur.com/pK9EIRV.png)
  >![](https://i.imgur.com/Io0Nn30.png)
  
  >OSPF在AS中,再用BGP讓AS跟AS之間傳遞

### Q4.
+ please give an example to show how BGP policy affects routing
  >![](https://i.imgur.com/LiRXiz1.png)
  >ABC are provider XYZ are customer. X不想經過B再到C所以不會通知B關於傳遞的事
### Q5.
+ 這個跟第三題有甚麼差啦 explain the operation of generalized forwarding




# Test3
### Q1.
+ A typical SDN controller consists of three layers: interface, network-wide state management, and communication. please describe their main functions.
  >interface:abstraction API
  >network-wide state management: state of networks link,switches, services : a distributed database
  >communication : communicate between SDN conrtoller and controlled switches
### Q2.
+ please describe the function of northbound and southbound API
  >northbound: SDN與高階component之間溝通
  >southbound: SDN與低階component之間溝通
  >![](https://i.imgur.com/h6xf8N1.png)

### Q3.
+ how does SDN overcome the limitation of traditional routing
  >define link weights so traffic routing algorithm computes routes accordingly
### Q4.
+ please explain the operation of traceroute based on ICMP error messages

### Q5.
+ what is the transport protocol of SNMP
  >UDP

# Test4
### Q1.
+ where is the link layer implemented
  >hosts and routers
### Q2.
+ given the data: 101110 and CRC generator 1001 please generate the CRC
  >101110000和1001用長除法做XOR的餘數
### Q3.
+ please list the pros and cons of embedding error correction bits in link-layer frames
  >pros:Error Detection and Correction bits
  >cons:not 100% reliable. it may miss some error
### Q4.
+ how does CSMA/CD minimize the collision probability in a broadcast channel
  >當收到別人的封包時,立即停止傳出封包
### Q5.
+ how does CSMA/CD minimize the collision period in a broadcast channel
  >當收到別人的封包時,立即停止傳出封包


# Test5
### Q1.
+ please describe the operation of exponential backoff in Ethernet 
  >![](https://i.imgur.com/0II74bk.png)


### Q2.
+ There are three types of MAC protocols: channel partitioning, random access and "taking turn". please dexcribe their pros and cons
  > :+1: channel partitioning 
  >divide channel into smaller pieces (time slots, frequency, code)
  >allocate piece to node for exclusive use
  
  > :+1:random access
  >channel not divided, allow collisions
  >recover from collisions
  
  > :+1:taking turn
  >nodes take turns, but nodes with more to send can take longer turns
### Q3.
+ please describe the purpose and operation of ARP.
  >解析網路層,透過IP來定位和得到MAC
  
### Q4.
+ ethermet preamble consist of seven "10101010" bytes followedby one "10101011" byte. what is the purpose of ethernet preamble
  >used to synchronize receiver, sender clock rates


### Q5.
+ how are the entries of an ethernet switch table generated
  >by self-learning

# Test 6
### Q1
+ please list three source of frame broadcasting in a Ethernet LAN with switches
  > address
  > type
  > CRC

### Q2
+ Please describe the purpose and operations of VLAN
  > let single physical switch operate as multiple virtual switches
  
### Q3
+ What is the function of VLAN trunk port
  >
### Q4
+ How can the frame transmission between two VLANs be achieved
  >use trunk port
### Q5
+ please list all possible protocols involed in a Web request from a newly connected laptop
  >DHCP,HTTP,TCP,UDP



---
---
---
-----
---
---
---
---

