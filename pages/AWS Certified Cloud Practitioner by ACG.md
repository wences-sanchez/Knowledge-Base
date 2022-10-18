tags:: ACloudGuru, AWS
deck:: [[ACloudGuru::AWS]]

- #tags #AWS #CCP-Exam
-
- ## 1. Introduction
	- The passing score is 7!
	- What is **cloud computing**, exactly?
		- Cloud computing is the **delivery of computing services** over the internet.
-
- ## 2. Foundations of Cloud Computing
	- Cloud9 is an example of [[PaaS]]
	- ### Leveraging the AWS Global Infrastructure
		- #### Regions
			- A [[region]] is a physical location in the world that contains AZs
			- Each [[region]] is **independent** and **isolated** from each other.
			- You can see that you previously have to select a region before doing any activity in AWS.
		- #### Availability Zones
			- The AZs are physically separated but connected through low-latency links
			- AZs Allow for high availability
			- If you distribute your application between AZs, you'll have HA.
		- #### Edge Locations
			- Edge locations reduce latency. They are used by **AWS CloudFront**
			- Regions > Availability Zones > Datacenters #flashcard
			  id:: 63454583-8fab-4d17-ad8c-819f4c634429
				- There are more **Edge Locations** than **Regions** and **AZs**.
	- ### Exploring your AWS Account
		- The regions are isolated.
			- That is why you cannot see the contents of a region in others' one.
		-
- ## 3. Technology
	- [[Index website]]
	-
	- ### Section Introduction
		- The different services are for different use cases. That's the reason why there are so many!
	- ### 3.2 Exploring Compute Services: EC2
		- EC2 is a foundational service used for managing our virtual instances.
			- 1. You're able to provision an EC2 instance at the click of a button
			  2. You can preconfigure it with an AMI template
			  3. You can deploy applications there
			  4. You have 750 hours/month in the free tier plan
		- You can use them to deploy a database or a web application
		-
		- #### Flashcards
		  collapsed:: true
			- Mention some characteristics of EC2 #flashcard
			  id:: 634d4173-6293-43a5-ba2a-1277991d6518
				- EC2 is a foundational service used for managing our virtual instances.
					- 1. You're able to provision an EC2 instance at the click of a button
					  2. You can preconfigure it with an AMI template
					  3. You can deploy applications there
					  4. You have 750 hours/month in the free tier plan
				- You can use them to deploy a database or a web application
		-
		- #### Ways of access an EC2 Instance #flashcard
		  id:: 634d3490-5a54-4dc2-8474-0335cbc84dc6
			- AWS Management Console
				- via a web browser
			- Secure Shell (SSH)
			- EC2 Instance Connect (EIC)
				- It removes the need to manage SSH keys
				- With EC2 Instance Connect, you use AWS Identity and Access Management (IAM) policies and principals to control SSH access to your instances, removing the need to share and manage SSH keys.
			- AWS Systems Manager
				- Allows to manage your EC2 instances via a web browser or the AWS CLI.
				- AWS Systems Manager es una solución segura de administración integral para entornos híbridos en la nube.
			-
		- #### EC2 Pricing Options #flashcard
		  id:: 634d3596-a583-4351-8c0a-d8ba06fb0a30
			- #### On-Demand
				- A fixed price in which you are billed down to the second based on the instance type. No contract.
				- Use it when:
					- You care about low cost without any upfront payment or long-term commitment.
					- Applications with unpredictable workloads that **can't** be interrupted
					- Your applications are under development
					- Your workloads will not run longer than a year
			- #### Spot
				- Your request of instances is fulfilled only if capacity is available.
				- Use it when:
					- You are not concerned about the **start** and **stop** of your application
					- Your workloads **can** be interrupted
			- #### Reserved Instances
				- RIs allow you to commit to a specific instance type in a particular region for 1 or 3 years.
			- #### Dedicated Hosts
				- Allow you to pay for a physical server that is fully dedicated to running your instances.
				- Use it when:
					- You want to bring your own server-bound software license from other vendors.
				- Don't confuse it with *reserved instances*
			- #### Savings Plans
		- An ELB distributes the traffic across multiple EC2 instances. Whereas the EC2 Auto Scaling feature adds or replaces EC2 instances (it scales them out).
			-
		- Scale out means to add or remove instances, whereas scale up means to upgrade an instance by adding more power (CPU, RAM) to an existing server.
	-
	- ### 3.3 Exploring Compute Services: EC2 in Action
	- ### 3.4 Exploring Compute Services: Lambda
		- What does *Serverless* mean? #flashcard
		  id:: 634d463b-2c50-4ce0-afd8-439cc0c83123
			- **Serverless** simply means that Amazon manages the servers for you and you cannot access them. You can pretend they don't exist.
		- Describe the pricing model of Lambdas #flashcard
		  id:: 634d4919-d3be-4a84-9a31-15c1861e36bf
			- **Compute time**: Pay only for compute time used. There is no charge if your code is not running
			- **Request count**: A request is counted each time it starts execution (including tests in the console).
			- **Always free**: Even after the free-usage tier expires, you'll have access to 1 million free Lambda calls each month.
	- ### 3.5 Create a Lambda Function using the AWS Management Console
		- You have to deploy your code before expecting it to succeed! #flashcard #dev-notes
	- ### 3.6 Exploring Compute Services: Additional Compute Services #flashcard
		- What is the use of containers?
			- To make our apps capable of executing again and again on different environments without worrying of machine specific configurations
		- #### AWS Fargate
			- Fargate allows you to manage containers.
			- It scales automatically and is **[[serverless]]** (means that you don't worry about provisioning, configuring or scaling servers)
		- #### Amazon Lightsail
			- It's similar to EC2, but for small projects. It allows you to quickly launch all the resources you need for small projects.
			- Deploy preconfigured applications, like *Wordpress* websites, at the click of a button
			- Lower predictable fees.
		- #### AWS Outposts
			- It allows you to run cloud services in your internal data center.
			- It supports workloads that need to remain on-premises due to latency or data sovereignty needs
			- AWS delivers and installs servers in your internal data center.
			- Used for a [[hybrid]] experience
			- Have access to the **cloud services** and **APIs** to develop apps **on-premises**.
		- #### AWS Batch
			- **Batch** allows you to process large workloads in smaller chunks (or batches).
			- Runs hundreds and thousands of smaller batch processing jobs
			- Dynamically provisions instances based on volume.
			- It works with other services as AWS Fargate, Amazon EC2 or spot instances.
	- ### 3.7 Leveraging Storage Services: S3
		- Companies collect lots of data because they need to analyze it and compare it over years.
		- #### Amazon S3
			- Objects are stored in buckets
				- Objects = files
				- Buckets = directories
			- Essentially unlimited storage that can hold millions of objects per bucket
			- Objects can be public or private
			- You can upload objects via the console, the CLI or with the SDKs.
		- #### A Closer look
			- You can set security at the bucket level or individual object level using ACLs, bucket policies or access point policies.
			- You can enable versioning to create multiple version of your file in order to protect against accidental deletion and to use a previous version.
			- You can use S3 access logs to track the access to your buckets and objects.
			- S3 is a **regional** service, but bucket names need to be globally unique.
		- #### Data Accessibility
			- **Durability**
			-
		-
		-
		-
		-
		-
		-
			-