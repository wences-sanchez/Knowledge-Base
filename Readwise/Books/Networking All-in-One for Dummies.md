# Networking All-in-One for Dummies

deck:: [[O'Reilly-Learning::Networking All-in-One for Dummies]]\
author:: [[Doug Lowe]]\
full-title:: "Networking All-in-One for Dummies"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781119471608/)
## Highlights
### Chapter 1: Welcome to Networking
- id:: 63c66a15-48e6-4bef-ae15-514f2e8b6599
   What is a network, for dummies? #flashcard 
    A network is nothing more than two or more computers connected by a cable or by a wireless radio connection so that they can exchange information.
-
- id:: 63c66a15-8749-4fa7-8777-457d049d17dc
   What is a network interface, for dummies? #flashcard 
    You can create a simple computer network by hooking together all the computers in your office with cables and using the computer’s network interface (an electronic circuit that resides inside your computer and has a special jack on the computer’s backside). Then you tweak a few simple settings in the computer’s operating system (OS) software, and — voilà!
-
- id:: 63c66a15-424d-4dba-bd96-6b0ae281f0a8
   How is a network cable different from a telephone cable? #flashcard 
    The type of network cable most commonly used is twisted-pair cable, so named because it consists of several pairs of wires twisted together in a certain way. Twisted-pair cable superficially resembles telephone cable. However, appearances can be deceiving. Most phone systems are wired using a lower grade of cable that doesn’t work for networks.
-
- id:: 63c66a15-816c-419b-9e23-578942b62e91
   What does packet mean in a network, for dummies? #flashcard 
    A packet is a message that’s sent over the network from one node to another node. The packet includes the address of the node that sent the packet, the address of the node the packet is being sent to, and data.
-
- id:: 63c66a15-e3af-4786-8c75-c2cb3e340781
   Who did computers work in a bus network? #flashcard 
    In a bus topology, every node on the network can see every packet that’s sent on the cable. Each node looks at each packet to determine whether the packet is intended for it. If so, the node claims the packet. If not, the node ignores the packet. This way, each computer can respond to data sent to it and ignore data sent to other computers on the network.
-
### Chapter 2: Network Infrastructure
- id:: 63c66a15-6f07-4bc6-b037-8081697fb982
   What is a network protocol, for dummies? #flashcard 
    A protocol provides a precise sequence of steps that each element of a network must follow to enable communications. Protocols also define the precise format of all data that is exchanged in a network. For example, the Internet Protocol (IP) defines the format of IP addresses: four eight-bit numbers called octets whose decimal values range from 0 to 255, as in 10.0.101.155.
-
- id:: 63c66a15-a4c6-4060-afe5-d72e4759bc56
   What is a network standard, for dummies? #flashcard 
    A standard is a detailed definition of a protocol that has been established by a standards organization and that vendors follow when they create products. Without standards, it would be impossible for one vendor’s products to work with another vendor’s.
-
- id:: 63c66a15-e942-48ce-9b71-e4a63f21af7b
   What is a network interface, for dummies? #flashcard 
    A network interface is the electronic circuitry that allows a device to connect to a network. Each network interface provides a port, which is the plug-in point for the interface. Generally speaking, the terms port and interface are synonymous.
-
- id:: 63c66a15-a927-4108-bbd8-00cd1d3a4c3b
   What does a MAC stand for? #flashcard 
    Every network interface must have a unique identifier called a MAC address. (MAC stands for media access control, but that won’t be on the test.) Each MAC address is unique throughout the entire world.
-
- id:: 63c66a15-00ee-4773-ae83-975b018dba45
   What is DHCP used for? #flashcard 
    Dynamic Host Configuration Protocol (DHCP), which allows computers that join a network to be assigned an IP address. When a network interface is first connected to a network, it sends out a broadcast message requesting the address of the network’s DHCP server. Every device on the network sees this packet. But only the DHCP service will respond.
-
- id:: 63c66a15-07b9-4a8d-8bd9-b5558e51f2ca
  
  However, mesh networks are common for metropolitan or wide area networks. These networks use routers to route packets from network to network. For reliability and performance reasons, routers are usually arranged in a way that provides multiple paths between any two nodes on the network in a mesh-like arrangement. #flashcard
-
- id:: 63c66a15-12bc-4534-9f15-708d540fdd09
  
  Usually a LAN is contained within a single building, but a LAN can extend to several buildings on a campus, provided that the buildings are close to each other (typically within 300 feet of each other, although greater distances are possible with special equipment). #flashcard
-
- id:: 63c66a15-0811-4c8f-9275-2e553e21e087
   About mesh networks on the internet #flashcard 
    Mesh networks aren’t very practical in a LAN setting. For example, to network eight computers in a mesh topology, each computer would have to have seven network interface cards, and 28 cables would be required to connect each computer to the seven other computers in the network. Obviously, this scheme isn’t very scalable.
     However, mesh networks are common for metropolitan or wide area networks. These networks use routers to route packets from network to network. For reliability and performance reasons, routers are usually arranged in a way that provides multiple paths between any two nodes on the network in a mesh-like arrangement.
-
- id:: 63c66a15-b85a-4f61-aef9-6d9a3382edd3
   How are MAC represented? #flashcard 
    MAC addresses are 48 bits in length, which means that more than 280 trillion devices can be assigned unique MAC addresses before we run out. When written, MAC addresses are written in six octets separated by hyphens. An octet is a group of eight binary bits, written as a two-digit number in hexadecimal notation, which uses the letters A through F in addition to the digits 0 through 9 to represent the value of each octet. A typical MAC address looks like this:
     48-2C-6A-1E-59-3D
-
- id:: 63c66a15-ed03-4180-802b-d41a58de2ace
   What is DHCP used for? #flashcard 
    One of the most common users of broadcast packets is Dynamic Host Configuration Protocol (DHCP), which allows computers that join a network to be assigned an IP address. When a network interface is first connected to a network, it sends out a broadcast message requesting the address of the network’s DHCP server. Every device on the network sees this packet. But only the DHCP service will respond.
-
### Chapter 3: Switches, Routers, and VLANs
- id:: 63c66a15-71a3-41e1-9b9a-0edcb74a3ab4
  
  the three basic functions of a switch:
     Learning: The switch learns what devices are reachable on each of its ports.
     Forwarding: The switch forwards incoming packets just to the correct port based on the intended destination.
     Flooding: The switch forwards incoming packets to all ports when it hasn’t yet learned how to reach the intended destination. #flashcard
-
- id:: 63c66a15-fe47-4fa2-bd85-5ab158cd80b8
   About ARP and its use #flashcard 
    You may be surprised to discover just how much broadcast traffic actually happens on a large network. The most common type of broadcast packet is an Address Resolution Protocol (ARP) request. ARP is the protocol used to determine the MAC address of a given IP address. If one IP device wants to send a packet to another IP device, the sender needs to know the MAC address of the recipient. So, the sender broadcasts an ARP request, which is essentially the question “Does anyone know the MAC address of this particular IP address? If so, please let me know.”
-
- id:: 63c66a15-eb16-4e9e-a14a-aa308b05a4a5
  
  the switches — which don’t know about IP addresses — must determine the MAC addresses not only of the sending and receiving computers, but also of the router. And the router must also know the MAC addresses of the two switches #flashcard
-
- id:: 63c66a15-aac7-41b4-935e-267fa93ea926
   Explain, basically, what NAT does. #flashcard 
    When a router is used to connect a private network to the Internet, one of the router’s most important functions is routing traffic from all the computers on the private side of the router to the public side, which usually has just a single public IP address. To accomplish this magic, the router uses network address translation (NAT).
     In short, when a computer on the private side of the network sends a packet through the router to the Internet, the router substitutes its own public IP address as the sender address, and keeps track of the fact that it sent a packet on behalf of a computer on the private side. When the recipient on the Internet receives the packet, it sees that the sender was the router. It then sends a response back to the router, which then substitutes the original sender’s private IP address for the destination address and forwards the packet to the correct computer on the private network.
-
- id:: 63c66a15-9225-4d62-af0d-b37ac28f62ea
   Explain what is a VPN. #flashcard 
    A virtual private network (VPN) is a secure connection between two private networks over a public network (in other words, over the Internet). All the data that flows over the VPN is encrypted, so anyone who steals packets from the VPN will find them unintelligible; only the parties on either end of the VPN are able to decrypt the packets.
     VPN connections are often called tunnels, because they provide an isolated pathway from one point to another through the Internet. The only way to gain meaningful access to a VPN tunnel is at either end.
     There are two common uses for VPNs:
     To provide remote workers with secure access to your company network: To do that, you set up a VPN on the router, and then provide your remote workers with the credentials necessary to access the VPN. The remote workers can run a software VPN client on their home computers or laptops to connect to your company network.
     To establish a tunnel directly between routers on two networks that are separated geographically: For example, suppose you have offices in Los Angeles and Las Vegas. You can use routers on both networks to establish a VPN tunnel between them. This effectively joins the networks together, so that devices on the Los Angeles network can freely exchange packets with devices on the Las Vegas network, and vice versa.
-
### Chapter 5: Cloud Computing
- id:: 63c66a15-c320-4d55-aa2b-78a54ffa7a9b
  
  Also referred to as Platform as a Service (PaaS), this class of service refers to providers that give you access to a remote virtual operating platform on which you can build your own applications. #flashcard
-
### Chapter 6: Running Apache
- id:: 63c66a15-83cf-4f5a-b6b9-ffd46e32fe8a
  
  Manually Editing Apache’s Configuration Files #flashcard
-