title:: Terraform: Allow All Internal Traffic Inside Aws Security Group (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "Terraform: Allow All Internal Traffic Inside Aws Security Group"
category:: #articles
url:: https://stackoverflow.com/questions/63001838/terraform-allow-all-internal-traffic-inside-aws-security-group

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- How can you allow inbound traffic from everywhere inside a security_group_rule in Terraform? .code .aws #flashcard
		  id:: 7464b644-2f75-4093-a8b7-16febbc67d3c
			- If your requirement is to allow all the traffic from internet you can use
			  
			    cidr_blocks      = ["0.0.0.0/0"] 
			    ipv6_cidr_blocks = ["::/0"]
	- -