# AWS: How to Allow All TCP Traffic Between All Instances in Same VPC?

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "AWS: How to Allow All TCP Traffic Between All Instances in Same VPC?"\
category:: #articles\
url:: https://stackoverflow.com/questions/42322445/aws-how-to-allow-all-tcp-traffic-between-all-instances-in-same-vpc\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63639904-6b2b-4657-8af2-4ce614e0162e
   How can you allow all traffic between instances in the same VPC? .aws #flashcard 
    to Allow any traffic between ALL servers in the VPC is not a good practice.
     you should rethink in your VPC purpose.
     Any way, if you want a group of servers to communicate with each other you can create a Security Group 
     And Assign it for all servers that you want.
     and in inbound rules you add one rule from type "All TCP" and the source of this rule will be the same Security Group.
     if your Security Group ID is 'sg-xxxxxxxx'
     then the rule will be like this:
     All TPC | TCP | 0-65535 | custom | sg-xxxxxxxx
-