title:: Readwise/Terraform: Allow All Internal Traffic Inside Aws Security Group (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "Terraform: Allow All Internal Traffic Inside Aws Security Group"
category:: #articles
url:: https://stackoverflow.com/questions/63001838/terraform-allow-all-internal-traffic-inside-aws-security-group

- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- -
		- How can you allow inbound traffic from everywhere inside a security_group_rule in Terraform? .code .aws #flashcard
			- If your requirement is to allow all the traffic from internet you can use
			  
			    cidr_blocks      = ["0.0.0.0/0"] 
			    ipv6_cidr_blocks = ["::/0"]
	- -