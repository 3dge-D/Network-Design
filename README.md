## **Network Design Proposal**

## **Part1**

##  I. Physical Network Design

**A. Network Topology**

University of Maryland University College is in the process of occupying
a new building. They are in need of a secure network infrastructure.
This building will have 11 classrooms, 7 offices, a library and computer
lab. With a growing concern for cybersecurity, UMUC wants to make sure
that all student, faculty and university data is protected. Therefore,
security will be a priority in this design. There will be 6 classroom
computer labs, each with 23 student computers, 1 computer for the
instructor and 1 computer used as a server for instructional use. There
will also be a computer in each office. The Admissions office will need
5 computers. Additionally, there will be a computer lab with 20
computers. In all, there will be a need for a total of 175 desktop
computers and 6 servers.

This will be a large network that will likely expand over time.
Therefore, the proper networking devices will need to be implemented to
support large amounts of traffic and an expanding network. High speeds,
strong security and a good amount of modularity will be key in this
design.

To support this large network there will need to be at least a 40 Mbps
connection and a backup connection of at least 20 Mbps. A public Wi-Fi
connection will also be needed for any visitors.

**Proposed Topology**

I am proposing an extended star topology for this network design. This
topology can cover larger distances and will be easy to implement in
this type of environment---a two story building with 186 computers and 2
server rooms. With this topology, it will be easy to locate points of
failure. \[1\] Additionally this topology will make it easy to expand
the network if needed.

![](https://i.imgur.com/pefxipO.jpg)

**B. Network Media**

**Business Needs**

Security is a high priority for UMUC. This campus will need cabling that
is fast, secure and reliable at long distances. With a 50-year-old
building, we can assume that there will be high amounts of
Electromagnetic Interference. We will need cabling that can withstand
high amounts of EMI. Shielded or Fiber cabling would be the only good
candidates in this particular network.

**Network Diagram** ![](https://i.imgur.com/nViszlj.jpg)![](https://i.imgur.com/rXIwhNV.jpg)

**Proposed Network Media**

Category 6a Shielded Twisted Pair Cabling (Cat 6a STP)

**Estimated Amount-** 4,000ft

**Estimated Cost**- \$1500 \[2\]

**Justification**

Cat 6a STP is highly reliable and fits well with this network design.
This building will have high network traffic with over 100 devices, so
data flow will be important. The twisted pair cabling will prevent
crosstalk, which will prevent issues with data flow and corruption. In
addition to high network traffic, there is expected to be a lot of
electromagnetic interference(EMI) due to the 50-year-old structure.
While Fiber cabling would completely eliminate this issue, it has a high
risk of breaking because of its glass core. We need the cabling to be
very flexible so that it can be ran through walls and around corners.
The foil shielding of the STP will greatly reduce EMI. It will also be
much more flexible than Fiber cabling. Cat 6a will also be very fast
over a long distance. The cable supports 10 Gigabit speeds up to 100
meters.

**C. Network Devices**

**Business Needs**

UMUC will need devices that enforce a secure network with high
performance. The campus will need network devices that can handle the
high network traffic. This network will need to be fast and expandable.
It will need to run Gigabit Ethernet(1000Base-T) to support the
stability and growth of the network. With high network traffic, comes
security vulnerabilities. This network will need secure communication
between devices as well as secure communications between the network and
the outside internet. Security protocols and features will be a priority
for each device. There will need to be public internet access.
Therefore, a Wireless Access Point(WAP) will serve this purpose. It will
need to be placed outside the DMZ to prevent any unwanted or malicious
activity from outside users.

**Proposed Network Devices**

-   **1 x Cisco ISR4331-V/K9 Router-** This will be the main network
    router that will communicate with the outside network. It will be
    located on the first floor in the server room. The Cisco
    ISR4331-V/K9 Router has features that will provide extra security
    for the network. \[3\] These features include IPSec: a protocol that
    will provide encryption, authentication and other security services
    in the network layer\[4\]

> **Estimated Cost: \$2700**\[5\]

-   **2 x Cisco SG300-52MP Layer 3 switches**- One switch will be in the
    first floor and another will be in the second floor. These switches
    will allow the different subnetworks to be divided into separate
    Virtual Local Area Networks (VLANs). Using VLANs will improve the
    performance of the network. Also with the ability to control which
    networks can communicate with each other, VLANs will improve
    security throughout the network. \[6\]

> **Estimated Cost: \$3000 (\$1500 ea.)**\[7\]

-   **9 x Cisco 200 Series SLM2048T-NA switches-** There will be one
    switch in each of the 6 classroom computer labs. Also, there will be
    one in the Library Computer Lab. Lastly there will be one for the
    first-floor offices and one for the second-floor offices.

> **Estimated Cost: \$5400 (\$600 ea.)**\[8\]

-   [**1x Cisco CISCO861W-GN-A-K9 Wirless Router-** This will be the WAP
    for Public Wifi.]{.mark}

> **[Estimated Cost:]{.mark}** **\$400**\[9\]

**Justification**

The proposed devices will provide extra security for the network through
IPsec and VLAN support. VLANs are devices that are configured to
communicate with each other as if they were on a physical network and
are based on logical connections. \[10\] With a Layer 3 switch we will
be able to create subnets using VLANs. This will allow us to isolate
classrooms and offices on their own networks and prevent any unwanted
communications or access between the subnets. Thus, a student in a
classroom will not have access to HR or Admissions. VLANs will add
protection for those within the network, and will improve performance
and manageability of each subnet.

The Cisco Wireless Router will provide public access to the internet for
visitors and students or faculty that want to connect other devices.

**D. Network Security Devices**

**Business Needs**

As stated, security is a high priority for UMUC. The school will be
responsible for personal information of many faculty and students. There
will be a need for protection from anyone trying to connect from outside
of the LAN as well as protection for those within the LAN. Also, data
that is sent out from the network will need to be protected with proper
encryption methods.

**Proposed Network Security Devices**

-   **1 x Cisco ASA 5525-X Firewall-** This firewall will be located on
    the first floor in the server room. It will be connected between the
    router and the layer 3 switches. Its features include an Intrusion
    Prevention System(IPS), Malware Protection, Virus Protection and
    Worm Scanning. \[11\]

> **Estimated Cost: \$3200**

**Justification**

The Cisco ASA 5525-X will provide the necessary security for the UMUC.
The IPS will protect the network from being compromised by outside
users. Also, the additional security from the router will encrypt any
data sent throughout the network. With communication encryption from the
Cisco ISR4331-V/K9 router, and IPS and malware/virus protection from the
Cisco ASA 5525-X firewall, security over the entire Local Area
Network(LAN) will be reliable and robust.

**E. Computer Systems**

**Business Needs**

UMUC will need a total of 155 desktop computers, 6 server computers for
instructional use, a DHCP server for IP addressing, a Database server to
hold student/faculty information, an Active Directory server for
username and password authentication, a file server, a DNS server and a
Web server. Each desktop computer will need to be fast and reliable.

**Proposed Computer Systems**

-   **6 x PowerEdge T330 Tower Servers-** These servers will be in each
    of the 6 classroom computer labs. They will be used for instruction.

> **Estimated Cost: \$7800(\$1300 ea.)**\[12\]

-   **155 x Dell Inspiron i3668-5168BLK Desktop Computers-** There will
    be 24 in each classroom computer lab, 20 in the library computer lab
    and 11 total in the offices (5 in the Admissions office**)**

> **Estimated Cost: \$93,000(\$600 ea.)**\[13\]

-   **Cisco C240 M4 2U Rack Server-** This server will be located on the
    first floor in the server room. The server will handle all the
    network services.

-   **Estimated Cost: \$6000**\[14\]

-   **Microsoft Windows Server Essentials 2016-** This is the most
    recent version of Windows Server OS. It will be installed on all 6
    classroom servers.

> **Estimated Cost: \$3600(\$600 ea.)**\[15\]

-   **Microsoft Windows 10 Professional 64-bit-** This will be installed
    on all office and classroom computers.

> **Estimated Cost: \$0(included with computer system)**

**Justification**

The PowerEdge T330 Servers will be good for instructional classroom use.
The instructional servers will have 16 GB of memory which will be plenty
of memory to run the necessary applications and service. The servers
will also have 8 hot swappable drive bays which will allow
expandability. The Cisco C240 Server will handle all of the network
service needs which include DHCP, DNS, and Active Directory. The
modularity of the Cisco server will allow for expansion as the network
expands.

The Dell Inspiron i3668-5168BLK Desktop Computers will feature 8GB of
memory, 1TB storage space and 3.0ghz Intel i5 CPUs. They will be fast
and reliable, and will be capable of handling the needs of the campus
students and faculty.

The Windows Server 2016 and Windows 10 Pro operating systems are the
most recent operating systems from Microsoft and have improved security.
They are widely used and will require minimal training.

**Total Estimated Cost**

  -----------------------------------------------------------------------
  **Device/Software**                       **Estimated Cost**
  ----------------------------------------- -----------------------------
  4000ft Cat6a STP Cabling                  \$1500

  1x Cisco ISR4331-V/K9 Router              \$2700

  2x Cisco SG300-52MP Layer 3 switch        \$3000

  9x Cisco 200 Series SLM2048T-NA switches  \$5400

  1x Cisco ASA 5525-X Firewall              \$3200

  1x [Cisco CISCO861W-GN-A-K9 Wireless      \$400
  Router]{.mark}                            

  6x PowerEdge T330 Tower Servers           \$7800

  155x Dell Inspiron i3668-5168BLK Desktop  \$93000
  Computers                                 

  1x Cisco C240 M4 2U Rack Server           \$6000

  6x Microsoft Windows Server Essentials    \$3600
  2016                                      

  Microsoft Windows 10 Professional 64-bit  \$0

  **Total**                                 **\$126,600**
  -----------------------------------------------------------------------

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## **References**

\[1\]K. Lawrence, \"Back to the Basics: Networks and
Topologies\", *Blog.boson.com*, 2013. \[Online\]. Available:
http://blog.boson.com/bid/87993/Back-to-the-Basics-Networks-and-Topologies.

\[2\]
http://www.monoprice.com/Product?p_id=13072&gclid=COjOiL-a_dACFdmCswodOPMH8w

\[3\]*Cisco Intelligent WAN powered by ISR 4000 Series*, 1st ed. Cisco,
p. 1.

\[4\]Y. Li-shen and R. Zheng-wei, \"Research of Cooperation of IPSec and
Firewall.\", *Proceedings of the Third International Symposium on
Computer Science and Computational Technology*, vol. 2, no. 1, pp.
422-425, 2010.

\[5\]
https://www.neweggbusiness.com/product/product.aspx?item=9b-33-150-523

\[6\] B. Mitchell, \"What a VLAN can do for you and your business
computer network\", *Lifewire*, 2016. \[Online\]. Available:
https://www.lifewire.com/virtual-local-area-network-817357.

\[7\]
[[https://www.neweggbusiness.com/Product/Product.aspx?Item=9B-33-420-403&nm_mc=KNC-GoogleBiz-PC&cm_mmc=KNC-GoogleBiz-PC-\_-pla-\_-Network+-+Switches-\_-9B-33-420-403&gclid=CNuH04PNiNMCFYKFswodSHQLBA]{.underline}](https://www.neweggbusiness.com/Product/Product.aspx?Item=9B-33-420-403&nm_mc=KNC-GoogleBiz-PC&cm_mmc=KNC-GoogleBiz-PC-_-pla-_-Network+-+Switches-_-9B-33-420-403&gclid=CNuH04PNiNMCFYKFswodSHQLBA)

\[8\]
[[https://www.neweggbusiness.com/product/product.aspx?item=9b-33-150-123]{.underline}](https://www.neweggbusiness.com/product/product.aspx?item=9b-33-150-123)

\[9\]
[[https://www.neweggbusiness.com/product/product.aspx?item=9b-33-120-274]{.underline}](https://www.neweggbusiness.com/product/product.aspx?item=9b-33-120-274)

\[10\]\"Understanding and Configuring VLANs\", Cisco. \[Online\].
Available:
http://www.cisco.com/c/en/us/td/docs/switches/lan/catalyst4500/12-2/25ew/configuration/guide/conf/vlans.html.
\[Accessed: 04- Apr- 2017\].

\[11\]\"Cisco ASA 5500-X Series Next Generation Firewalls Data
Sheet\", *Cisco*, 2016. \[Online\]. Available:
http://www.cisco.com/c/en/us/products/collateral/security/asa-5500-x-series-next-generation-firewalls/data-sheet-c78-729807.html.

\[12\]
https://www.neweggbusiness.com/product/product.aspx?item=9b-59-155-432

\[13\]
[[https://www.neweggbusiness.com/product/product.aspx?item=9b-83-163-367]{.underline}](https://www.neweggbusiness.com/product/product.aspx?item=9b-83-163-367)

\[14\]
[[https://www.neweggbusiness.com/product/product.aspx?item=9b-2ns-001d-001y5]{.underline}](https://www.neweggbusiness.com/product/product.aspx?item=9b-2ns-001d-001y5)

\[15\]
[[https://www.microsoftstore.com/store/msusa/en_US/pdp/Windows-Server-2016-Essentials/productID.5074016900]{.underline}](https://www.microsoftstore.com/store/msusa/en_US/pdp/Windows-Server-2016-Essentials/productID.5074016900)

## **Network Design Proposal**

## **Part 2**

**II. Network Addresses Design**

**A. Subnetting**

**Methodology**

This network has been assigned the 199.1.2.0 network address. It will be
divided into 8 subnets with 25 host per subnet. Dividing the network
into subnets will improve performance and security. It will also allow
for more efficient management.

With a subnet mask of 255.255.255.0, the network will be subnetted as
follows:

  ------------------------------------------------------------------------
  **Subnet**      **Network        **Host Address        **Broadcast
                  Address**        Range**               Address**
  --------------- ---------------- --------------------- -----------------
  Subnet Mask:                                           
  255.255.255.0                                          

  Classroom 1     199.1.2.0        199.1.2.1 -           199.1.2.31
                                   199.1.2.30            

  Classroom 2     199.1.2.32       199.1.2.33 -          199.1.2.63
                                   199.1.2.62            

  Classroom 3     199.1.2.64       199.1.2.65 -          199.1.2.95
                                   199.1.2.94            

  Classroom 4     199.1.2.96       199.1.2.97 -          199.1.2.127
                                   199.1.2.126           

  Classroom 5     199.1.2.128      199.1.2.129 -         199.1.2.159
                                   199.1.2.158           

  Classroom 6     199.1.2.160      199.1.2.161 -         199.1.2.191
                                   199.1.2.190           

  Library Lab     199.1.2.192      199.1.2.193-          199.1.2.223
                                   199.1.2.222           

  Office Network  199.1.2.224      199.1.2.225 -         199.1.2.255
                                   199.1.2.254           
  ------------------------------------------------------------------------

##  

##  

##  

## **Network Design Proposal**

## **Part 3**

**III. Network Services Design**

**A. Network Services**

**Business Needs**

This UMUC campus will need various network services to accommodate the
needs of the faculty and students. There will be a need for a DHCP
server for IP addressing. A DNS server will be needed for domain name
resolution. A file server will be needed to hold documents and resources
for faculty and student use. An Active Directory will be needed for
username and password authentication for all personnel. Lastly a
database server will be needed to store faculty and student information.

**Proposed Network Services**

The proposed network services are as follows:

DHCP

DNS

File

Active Directory

Database

**Justification**

There will be over 100 devices in this network. Therefore, a DHCP server
will be very beneficial for assigning IP addresses automatically and
will save a lot of time and money. A DNS server will domain name
resolution. This will allow for easier access to domains by not having
to remember long IP addresses. File and Database servers will be used to
store student and faculty information as well as any documentation and
resources in a central location, and will be easily access by authorized
users. An Active Directory Server will be used for username and password
authentication. This will allow any authorized users to have access to
the network with proper credentials while not allowing those without
authorization, access to the network.

**B. Network Security Measures**

**Business Needs**

This campus will service several faculty and staff as well as over 100
students and guest. The network will need to be capable of securing
personal data that will be kept away from hackers or malicious users.
The proper security measures will need to be taken to ensure the safety
of all data. There will be a need for fault management and network
monitoring tools to provide the automated detection and response of
network issues.

**Proposed Network Security Measures**

The proposed Network Security Measures are as follows:

**Training**

All faculty, staff and students will need training to ensure the
security of personal information. All staff will need to be trained on
various methods of keeping information secure. These methods include
creating a secure password, not giving out sensitive or personal
information such as usernames and passwords, and recognizing and
avoiding malicious links and emails. All of this information will need
to be documented. The staff will then be required to train new student
users before they are given access to the network.

**Monitoring**

This network will utilize the network monitoring tools provided by the
**Cisco ISR4331-V/K9 Router.** These tools include:

· **SNMP (Simple Network Management Protocol)**

· **IPsec**

**Justification**

The proper training of all personnel will be the most important security
measure implemented in this network. Ensuring all users utilize systems
properly and are educated on the importance of password complexity will
greatly increase the security of the network and improve user data
protection.

The Simple Network Management Protocol can be used to collect
information and monitor activity from the various devices on the
network.\[1\] This will allow the network admin to keep up with activity
on the network. IPsec will be used to encrypt and authenticate packets
of data sent across the network.\[2\] This will protect the privacy of
all data sent throughout the network.

**References**

> \[1\]\"What Is SNMP?: Simple Network Management Protocol (SNMP)\",
> *Technet.microsoft.com*, 2017. \[Online\]. Available:
> https://technet.microsoft.com/en-us/library/cc776379(v=ws.10).aspx.
>
> \[2\]\"What Is IPSec?: Security Policy; Security Services\",
> *Technet.microsoft.com*, 2017. \[Online\]. Available:
> https://technet.microsoft.com/en-us/library/cc776369(v=ws.10).aspx.
