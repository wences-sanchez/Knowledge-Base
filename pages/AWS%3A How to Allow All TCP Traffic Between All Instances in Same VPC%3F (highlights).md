title:: AWS: How to Allow All TCP Traffic Between All Instances in Same VPC? (highlights)
author:: [[stackoverflow.com]]
full-title:: "AWS: How to Allow All TCP Traffic Between All Instances in Same VPC?"
category:: #articles
url:: https://stackoverflow.com/questions/42322445/aws-how-to-allow-all-tcp-traffic-between-all-instances-in-same-vpc

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- How can you allow all traffic between instances in the same VPC? .aws #car
	  id:: 634014ed-b6e7-4f0d-a3b6-3a2fcf39b863
		- to Allow any traffic between ALL servers in the VPC is not a good practice.
		  you should rethink in your VPC purpose.
		  
		  Any way, if you want a group of servers to communicate with each other you can create a Security Group 
		  
		  And Assign it for all servers that you want.
		  
		  and in inbound rules you add one rule from type "All TCP" and the source of this rule will be the same Security Group.
		  
		  if your Security Group ID is 'sg-xxxxxxxx'
		  then the rule will be like this:
		  
		  All TPC | TCP | 0-65535 | custom | sg-xxxxxxxx
	- -