title:: Networking Fundamentals (highlights)
deck:: [[Other-Books::Networking Fundamentals]]
author:: [[]]
full-title:: "Networking Fundamentals"
category:: #books

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Firewalls
		- -
			- About what a firewall is. #flashcard
				- As a basic description, a firewall is designed to either allow or deny network traffic based upon a set of defined criteria. These criteria could be a predefined set of default rules or could be user-created, or even a combination of the two. These rules are often referred to as access control entries (ACEs), and a group of them form an access control list (ACL). These criteria could then be applied to outbound (or egress) traffic or inbound (or ingress) traffic. Understanding that a rule can be applied in each direction is important to know. For example, you may be troubleshooting a connectivity problem between two devices, so you would use the commonly used ICMP tool known as ping since ICMP can be used for malicious purposes and Windows Firewall blocks it by default.
		- -
		- -
			- About **network-based firewalls** and **host-based firewalls** #flashcard
				- you may be thinking that a network-based firewall is the better of the two as it protects the entire network. However, look at the following diagram and pay particular attention to the placement of the firewall. It's only inspecting traffic that transits through it. But what would happen if Computer A was compromised? If we only had a network-based firewall in place, there is nothing preventing Computer A from attacking Computer B:
				  
				  
				  Figure 1.3: Network-based firewall
				  So, is a host-based firewall better? It would certainly prevent the preceding issue where Computer A attacks Computer B, but it leaves your network susceptible to an attack from outside. You may be thinking, that's OK, because the host-based firewalls would protect the systems. That may be correct for some systems, but not all network devices have the capability to have a host-based firewall. A lot of IoT devices are prime examples of this. Because of this, it is recommended that any network you run has both host-based and network-based firewalls to provide what is known as defense in depth.
		- -
	- DMZ
		- -
			- What does **DMZ** stand for?
			  Figure 1.5 #flashcard
				- A DMZ, or a perimeter network, is a means of allowing the public to access certain network services while still maintaining the security of your internal devices. At this point, you may be thinking, that's what an extranet does. Yes, there are some similarities between them, but, remember, an extranet provides access to those services to trusted organizations, whereas a DMZ allows access to the public. No trust or authorization is required.
				  
				  Obviously, making anything accessible to the public brings with it inherent security risks, so it is important that only services that are deemed as public-facing and necessary are placed there and that suitable security mechanisms are put in place as added protection.
		- -
	- Hostnames
		- -
			- A computer's hostname is an easy-to-read (for humans) method of identifying a device on the network. Each device's hostname is configured by the system administrator. The hostname may be reflective of the role that the device is performing; for example, MXServer for a mail exchange server, DC1 for a domain controller, and so on. They may follow a set naming convention; I have worked in organizations that name file servers after Star Wars characters, and print servers after Star Trek characters. This is useful if everyone is a fan of these two movie and TV franchises. #flashcard
		- -
	- IP addresses
		- -
			- About IPs structure #flashcard
				- An IPv4 address is broken down into two sections:
				  
				  A network element
				  A host element
				  The network element is used as a means of identifying the network a device is on, while the host element identifies the device itself on the network. This provides a hierarchical approach to addressing.
		- -
	- Peer-to-peer networks
		- -
			- A P2P network (sometimes referred to as a workgroup) is one where there is no one device that has complete control of the network and the files, services, and so on that are used on the network. The term peer refers to individuals #flashcard
		- -
	- Virtual LANs
		- -
			- Figure 2.25: Example VLAN in a hospital #flashcard
		- -