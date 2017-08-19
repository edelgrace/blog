---
title: CCNA1 8.2.1.4 Packet Tracer – Designing and Implementing a VLSM Addressing Scheme
author: Edel
type: post
date: 2016-06-04T06:07:31+00:00
url: /life/ccna1-8-2-1-4-packet-tracer-designing-and-implementing-a-vlsm-addressing-scheme/
categories:
  - Technology
tags:
  - CCNA

---
I'm currently taking the CCNA1 course offered by Cisco. I struggled a lot with this activity so I thought it would be good to share how I finally figured it out. If you're a little lazy and just want the answers, click [here][1] to go straight to the addressing table or [here][2] to download the PDF. Be aware that the addresses may vary but the process is the same regardless.

I am only human and will make mistakes so do not hesitate to point out any errors!

<div class="panel">
  <ul>
    <li>
      <a href="#1">Part 1</a> <ul>
        <li>
          <a href="#1-1">Step 1</a>
        </li>
        <li>
          <a href="#1-2">Step 2</a>
        </li>
      </ul>
    </li>
    
    <li>
      <a href="#2">Part 2</a> <ul>
        <li>
          <a href="#2-1">Step 1</a>
        </li>
        <li>
          <a href="#2-2">Step 2</a>
        </li>
        <li>
          <a href="#2-3">Step 3</a>
        </li>
      </ul>
    </li>
    
    <li>
      <a href="#3">Part 3</a>
    </li>
  </ul>
</div>

### <a name="1"></a>Part 1: Examine the Network Requirements

#### <a name="1-1"></a>Step 1: Determine the number of subnets needed.

You will subnet the network address 192.168.72.0/24. The network has the following requirstrongents:

  * ASW-1 LAN will require 7 host IP addresses
  * ASW-2 LAN will require 15 host IP addresses
  * ASW-3 LAN will require 29 host IP addresses
  * ASW-4 LAN will require 58 host IP addresses

##### How many subnets are needed in the network topology?

[<img src="http://scattered.me/wp-content/uploads/2016/06/8.png" alt="8" width="571" height="358" class="alignnone size-full wp-image-11245" srcset="http://erzadel.net/blog/wp-content/uploads/2016/06/8.png 571w, http://erzadel.net/blog/wp-content/uploads/2016/06/8-300x188.png 300w" sizes="(max-width: 571px) 100vw, 571px" />][3]

**5 subnets are needed.** If you look at the topology, there are 4 LANs (coloured in orange) and 1 serial connection between Building1 and Building2. Therefore, you need 5 subnets.

#### <a name="1-2"></a>Step 2: Determine the subnet mask information for each subnet.

The original subnet mask of the network address is 255.255.255.0. This comes from the prefix length /24, which indicates that there are 24 bits set in the subnet mask. We will use this as the basis for subnetting. 

<table>
  <tr>
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      00000000
    </td>
  </tr>
  
  <tr>
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      00000000
    </td>
  </tr>
</table>

##### a. Which subnet mask will accommodate the number of IP addresses required for ASW-1?

**255.255.255.240 with a prefix length of /28.**

First, calculate the number of host bits that will be able to contain at least 7 hosts. \(2^n-2\\


  
= 2^4 &#8211; 2\\
  
= 14 usable >= 7 required\) 

14 is greater than 7, so this gives 4 bits are not set in the subnet mask.

<table>
  <tr>
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      240
    </td>
  </tr>
  
  <tr>
    <td>
      128+64+32+16+8+2+1
    </td>
    
    <td>
      128+64+32+16+8+2+1
    </td>
    
    <td>
      128+64+32+16+8+2+1
    </td>
    
    <td>
      128+64+32+16
    </td>
  </tr>
  
  <tr>
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11110000
    </td>
  </tr>
</table>

##### How many usable host addresses will this subnet support?

**14**. This comes from the formula in the previous question.

##### b. Which subnet mask will accommodate the number of IP addresses required for ASW-2?

**255.255.255.224 with a prefix length of /27.** \(2^n-2\\


  
= 2^5 &#8211; 2\\
  
= 30 usable >= 15 required\) 

<table>
  <tr>
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      224
    </td>
  </tr>
  
  <tr>
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11100000
    </td>
  </tr>
</table>

##### How many usable host addresses will this subnet support?

**30.**

##### c. Which subnet mask will accommodate the number of IP addresses required for ASW-3?

**255.255.255.224 with a prefix length of /27.** \(2^n-2\\


  
= 2^5 &#8211; 2\\
  
= 30 usable >= 29 required\) 

<table>
  <tr>
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      224
    </td>
  </tr>
  
  <tr>
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11100000
    </td>
  </tr>
</table>

##### How many usable host addresses will this subnet support?

**30.**

##### d. Which subnet mask will accommodate the number of IP addresses required for ASW-4?

**255.255.255.192 with a prefix length of /26.** \(2^n-2\\


  
= 2^6 &#8211; 2\\
  
= 62 usable >= 58 required\) 

<table>
  <tr>
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      224
    </td>
  </tr>
  
  <tr>
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11000000
    </td>
  </tr>
</table>

##### How many usable host addresses will this subnet support?

**62.**

##### e. Which subnet mask will accommodate the number of IP addresses required for the connection between Building1 and Building2?

**255.255.255.2552 with a prefix length of /30.**

We can use one subnet for the WAN. Since there are only two routers involved, we just need two addresses for this subnet. \(2^n-2\\


  
= 2^2 &#8211; 2\\
  
= 2 usable >= 2 required\) 

<table>
  <tr>
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      255
    </td>
    
    <td>
      252
    </td>
  </tr>
  
  <tr>
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11111111
    </td>
    
    <td>
      11111100
    </td>
  </tr>
</table>

### <a name="2"></a>Part 2: Design the VLSM Addressing Schstronge

#### <a name="2-1"></a>Step 1: Divide the 192.168.72.0/24 network based on the number of hosts per subnet.

##### a. Use the first subnet to accommodate the largest LAN.

**192.168.72.0/26.** The largest LAN is ASW-4 with 58 hosts. Subnet 192.168.72.0/24 into 192.168.72.0/26. This will give us 4 subnets (\(2^2 = 4\)) with 64 hosts per subnet.

The subnets are:

  * 192.168.72.0
  * 192.168.72.64
  * 192.168.72.128
  * 192.168.72.192

Since the subnets each contain 64 hosts, simple add 64 to the last octet. This method will not be as feasible for subnets with a large number of hosts. Another way is to convert everything to binary. Only the first 2 bits will change while the rstrongaining 6 bits stay the same.

<table>
  <tr>
    <td>
      192.168.72.0
    </td>
    
    <td>
      110000.10101000.01001000.<strong>00</strong>000000
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.64
    </td>
    
    <td>
      110000.10101000.01001000.<strong>01</strong>000000
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.128
    </td>
    
    <td>
      110000.10101000.01001000.<strong>10</strong>000000
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.192
    </td>
    
    <td>
      110000.10101000.01001000.<strong>11</strong>000000
    </td>
  </tr>
</table>

##### b. Use the second subnet to accommodate the second largest LAN.

**192.168.72.64/27.**. We are using the second subnet because we are reserving the first subnet for the ASW-4 network. The second largest LAN is ASW-3 with 29 hosts. Subnet 192.168.72.62/26 into 192.168.72.62/27. This will give 2 subnets (\(2^1 = 2\)) with 32 hosts per subnet. We use \(2^1\) because the base is /26 and /27 is only one bit longer.

The subnets are:

  * 192.168.72.64
  * 192.168.72.96

<table>
  <tr>
    <td>
      192.168.72.64
    </td>
    
    <td>
      110000.10101000.01001000.01<strong></strong>00000
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.96
    </td>
    
    <td>
      110000.10101000.01001000.01<strong>1</strong>00000
    </td>
  </tr>
</table>

##### c. Use the third subnet to accommodate the third largest LAN.

**192.168.72.96/27.** The third largest LAN is ASW-2 with 15 hosts. In the previous question, we already have 2 subnets that have 32 addresses each. The second subnet will be able to accomodate ASW-2. So we do not need to subnet further.

##### d. Use the fourth subnet to accommodate the fourth largest LAN.

**192.168.72.128/28.** Subnet 192.168.72.128/26 into 192.168.72.128/28. This will give 4 subnets (\(2^2 = 4\)) with 16 hosts per subnet. We use \(2^2\) because the base is /26 and /28 is two bits longer.

The subnets are:

  * 192.168.72.128
  * 192.168.72.144
  * 192.168.72.160
  * 192.168.72.176

<table>
  <tr>
    <td>
      192.168.72.128
    </td>
    
    <td>
      110000.10101000.01001000.10<strong>00</strong>0000
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.144
    </td>
    
    <td>
      110000.10101000.01001000.10<strong>01</strong>0000
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.160
    </td>
    
    <td>
      110000.10101000.01001000.10<strong>10</strong>0000
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.176
    </td>
    
    <td>
      110000.10101000.01001000.10<strong>11</strong>0000
    </td>
  </tr>
</table>

##### e. Use the fifth subnet to accommodate the connection between Building1 and Building2.

**192.168.72.145/30 and 192.168.72.146/30.** Subnet 192.168.72.144/28 into 192.168.72.144/30. This will give 4 subnets (\(2^2 = 4\)) with 2 hosts per subnet.

The subnets are:

  * 192.168.72.144
  * 192.168.72.148
  * 192.168.72.152
  * 192.168.72.156

<table>
  <tr>
    <td>
      192.168.72.144
    </td>
    
    <td>
      110000.10101000.01001000.1001<strong>00</strong>00
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.148
    </td>
    
    <td>
      110000.10101000.01001000.1001<strong>01</strong>00
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.152
    </td>
    
    <td>
      110000.10101000.01001000.1001<strong>10</strong>00
    </td>
  </tr>
  
  <tr>
    <td>
      192.168.72.156
    </td>
    
    <td>
      110000.10101000.01001000.1001<strong>11</strong>00
    </td>
  </tr>
</table>

#### <a name="2-2"></a>Step 2: Document the VLSM subnets.

Complete the Subnet Table, listing the subnet descriptions (e.g. ASW-1 LAN), number of hosts needed, then network address for the subnet, the first usable host address, and the broadcast address. Repeat until all addresses are listed.

##### Subnet Table

| Subnet Description | Number of Hosts Needed | Network Address/CIDR | First Usable Host Address | Broadcast Address |
| ------------------ | ---------------------- | -------------------- | ------------------------- | ----------------- |
| ASW-1 LAN          | 7                      | 192.168.72.128/28    | 192.168.128.129           | 192.168.128.143   |
| ASW-2 LAN          | 15                     | 192.168.72.64/27     | 192.168.72.65             | 192.168.72.95     |
| ASW-3 LAN          | 29                     | 192.168.72.96/27     | 192.168.72.97             | 192.168.72.127    |
| ASW-4 LAN          | 58                     | 192.168.72.0/26      | 192.168.72.1              | 192.168.72.63     |
| Serial WAN         | 2                      | 192.168.72.144/30    | 192.168.72.145            | 192.168.72.147    |

#### <a name="2-3"></a>Step 3: Document the addressing schstronge.

##### a. Assign the first usable IP addresses to Building1 for the two LAN links and the WAN link.

  * ASW-1 LAN: 192.168.72.129
  * ASW-2 LAN: 192.168.72.97
  * Serial WAN: 192.168.72.145

##### b. Assign the first usable IP addresses to Building2 for the two LANs links. Assign the last usable IP address for the WAN link.

  * ASW-3 LAN: 192.168.72.65
  * ASW-4 LAN: 192.168.72.1
  * Serial WAN: 192.168.72.146

##### c. Assign the second usable IP addresses to the switches.

  * ASW-1: 192.168.72.130
  * ASW-2: 192.168.72.98
  * ASW-3: 192.168.72.66
  * ASW-4: 192.168.72.2

##### d. Assign the last usable IP addresses to the hosts.

  * Host-A: 192.168.72.142
  * Host-B: 192.168.72.94
  * Host-C: 192.168.72.126
  * Host-D: 192.168.72.62

### <a name="3"></a>Part 3: Assign IP Addresses to Devices and Verify Connectivity

Now it's just a matter of plugging in values into Packet Tracer if you haven't already.

### <a name="answers"></a>Addressing Table

<td rowspan="3">
  Remote-Site 1
</td>

<td rowspan="3">
  Remote-Site 2
</td>

| Device | Interface      | IP Address      | Subnet Mask     | Default Gateway |
| ------ | -------------- | --------------- | --------------- | --------------- |
| G0/0   | 192.168.72.129 | 255.255.255.240 | N/A             |
| G0/1   | 192.168.72.97  | 255.255.255.224 | N/A             |
| S0/0/0 | 192.168.72.145 | 255.255.255.252 | N/A             |
| G0/0   | 192.168.72.65  | 255.255.255.224 | N/A             |
| G0/1   | 192.168.72.1   | 255.255.255.192 | N/A             |
| S0/0/0 | 192.168.72.146 | 255.255.255.252 | N/A             |
| SW1    | VLAN 1         | 192.168.72.130  | 255.255.255.240 | 192.168.72.129  |
| SW2    | VLAN 1         | 192.168.72.98   | 255.255.255.224 | 192.168.72.97   |
| SW3    | VLAN 1         | 192.168.72.66   | 255.255.255.224 | 192.168.72.65   |
| SW4    | VLAN 1         | 192.168.72.2    | 255.255.255.192 | 192.168.72.1    |
| User-1 | NIC            | 192.168.72.142  | 255.255.255.240 | 192.168.72.129  |
| User-2 | NIC            | 192.168.72.126  | 255.255.255.224 | 192.168.72.97   |
| User-3 | NIC            | 192.168.72.94   | 255.255.255.224 | 192.168.72.65   |
| User-4 | NIC            | 192.168.72.62   | 255.255.255.192 | 192.168.72.1    |




 [1]: #answers
 [2]: http://scattered.me/wp-content/uploads/2016/06/8.2.1.4-Packet-Tracer-Designing-and-Implementing-a-VLSM-Addressing-Scheme.pdf
 [3]: http://scattered.me/wp-content/uploads/2016/06/8.png