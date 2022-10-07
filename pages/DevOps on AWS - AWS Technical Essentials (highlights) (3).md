title:: DevOps on AWS - AWS Technical Essentials (highlights) (3)
author:: [[coursera.org]]
full-title:: "DevOps on AWS - AWS Technical Essentials"
category:: #articles
url:: https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/gcHiT/exercise-3-launch-the-employee-directory-application-on-amazon-ec2
tags:: Coursera

- #tags #Coursera
- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- A container is a standardized unit that packages up your code and all of its dependencies. This package is designed to run reliably on any platform, because the container creates its own independent environment. This makes it easy to carry workloads from one place to another, such as from development to production or from on-premises to the cloud. #spaced
	- -
	- -
	- You might be wondering: “Wouldn’t this block all EC2 instances from receiving the response of any customer requests?” Well, security groups are stateful, meaning they will remember if a connection is originally initiated by the EC2 instance or from the outside and temporarily allow traffic to respond without having to modify the inbound rules. #spaced
	- -
	- -
	- AWS Fargate, which we mentioned briefly earlier, is a serverless compute platform that you can run either ECS or EKS on top of. Previously, you learned that ECS and EKS run on clusters of EC2 instances. And in that case, you are using EC2 as the compute platform for your containers, and you also have tight control over those instances. With AWS Fargate as the compute platform, you run your containers on a managed serverless compute platform. The scaling and fault-tolerance is built in and you don't need to worry about the underlying operating system or the environment. #spaced
	- -