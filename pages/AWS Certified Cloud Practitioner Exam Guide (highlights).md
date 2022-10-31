title:: AWS Certified Cloud Practitioner Exam Guide (highlights)
deck:: [[O'Reilly-Learning::AWS Certified Cloud Practitioner Exam Guide]]
author:: [[]]
full-title:: "AWS Certified Cloud Practitioner Exam Guide"
category:: #books

tags:: AWS O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Chapter 1: What Is Cloud Computing?
	  collapsed:: true
		- -
		- What is known as cloud computing? #flashcard
		  id:: 0e525953-21f2-4697-9448-e22130ef080f
			- Cloud computing is a term used to describe the on-demand access to IT services that comprise compute, network, storage, and software services from third-party suppliers, usually via the public internet or some form of direct wide-area network (WAN) access. Companies can provision necessary IT applications for their organization without having to procure and manage their own infrastructure to host those applications. Instead, they lease/rent the required IT infrastructure from such third-party providers.
		- -
		- -
		- What is known as cloud computing? #flashcard
		  id:: 8d32817e-9b5f-46f7-89ac-a118d3e818be
			- Cloud computing is a term used to describe the on-demand access to IT services that comprise compute, network, storage, and software services from third-party suppliers, usually via the public internet or some form of direct wide-area network (WAN) access. Companies can provision necessary IT applications for their organization without having to procure and manage their own infrastructure to host those applications. Instead, they lease/rent the required IT infrastructure from such third-party providers.
			  
			  Cloud computing has existed for many years in some form, since the invention of the internet. In the old days, Hotmail (first launched in 1996 and now branded as Microsoft Outlook) was a prime example of early cloud computing. You could set up email accounts for your colleagues and yourself on Hotmail and use them to communicate. An alternative would be to host your own email servers' (the infrastructure) network connectivity, as well as the email application (the email software). This would ultimately mean additional costs as well as management overheads to maintain the email servers you hosted.
			  
			  Today, cloud computing has become mainstream and is, in several cases, the default option for many companies and start-ups. Currently, Amazon Web Services (AWS) is the largest provider of cloud computing services, offering a variety of cloud IT services in the form of infrastructure, platform, and software solutions.
		- -
		- -
		- Mention the 6 *advantages* of **cloud computing** #flashcard
		  id:: ff51262e-cbd9-48a5-82ea-52dbdb98519f
			- **1).** With cloud computing, you pay for the same infrastructure components only as and when you consume them. This on-demand, pay-as-you-go model also means that you save costs when you are not utilizing resources.
			  
			  The shift away from capital expense (CAPEX) for variable expense, also known as operating expense (OPEX), means that you can direct your precious business capital to more important areas of investment, such as developing new products or improving your marketing strategy.
			-
			- **2).** Benefit from massive economies of scale:
			-
			- **3).** Stop guessing capacity: Traditionally, while carrying out capacity planning, you would procure necessary hardware components for future growth. Predicting future growth is extremely difficult, and this often meant that you would overprovision your environment. The result would be expensive idle resources simply going to waste.
			-
			- **4).** Increase speed and agility: Cloud vendors such as AWS enable you to launch and configure new IT resources in a few mouse clicks—for example, you can provision a new fleet of servers for your developers within minutes, allowing your organization to exponentially increase its agility in building infrastructure and launching applications
			-
			- **5).** Stop spending money running and maintaining data centers: Hosting your own on-premises infrastructure consumes several hidden costs. In addition to using up precious capital to purchase expensive hardware, you also need a team of engineers to efficiently configure every infrastructure component and lease necessary real estate to rack, stack, and then power up your servers. You would also be required to keep the servers cool with appropriate air-conditioning systems—and that's not all. You would also have to spend money on expensive maintenance contracts to handle the wear and tear of the hardware.
			- 6th advantage of cloud computing #flashcard
			  id:: b8f3bace-7417-44c8-b426-31dc3d10e1a9
				-
				- Go global in minutes: AWS host their data centers in various regions across the globe. Although you may be based in one country, you will have complete access to all regions. This will help you offer lower latency and a superior customer experience, regardless of where your customers are located. Hosting copies of your resources in additional regions can also help you design for disaster recovery (DR) and business continuity requirements.
		- -
		- -
		- What is a hypervisor? #flashcard
		  id:: f09f15aa-6efa-481c-b0d5-e8a328d70158
			- A hypervisor is essentially a piece of software that sits between the actual physical hardware and the VMs. It is responsible for enabling the operating systems and applications running on those VMs to access the resources of the physical hardware in a manner that is controlled and that isolates the resources from each other. The hypervisor and its associated management software are used to carve out virtualized representations of the physical hardware components into smaller virtual components, which are then presented as VMs. Each VM can then have its own operating system installed, along with any required applications.
		- -
		- -
		- About virtualization and cloud computing. #flashcard
		  id:: ad1427a5-9041-4e70-ba3a-2bf498a6b163
			- One of the primary characteristics of a cloud computing provider is the ability to provision virtualized infrastructure resources using a self-service management tool. AWS offers such tools in the form of its Management Console (accessible via a web browser), command-line interface (CLI), and direct access to its software application programming interfaces (APIs), to enable customers to provision their resources such as servers, network, storage, and databases.
		- -
		- -
		- What is PaaS? #flashcard
		  id:: b348401a-736b-40bf-84f1-7d77df56ab1f
			- Platform as a Service (PaaS) is another cloud computing model designed to remove the burden of configuring and managing underlying infrastructure resources such as compute, storage, and network services. PaaS is designed to allow your organization to focus on developing your application code and offers you a platform to deploy and manage your application releases, updates, and upgrades.
			  
			  As your developers deploy their application code on the PaaS environment, the provider provisions the infrastructure required to support the application. This will include the necessary network architecture, firewall rules, storage, compute services, operating system management, and runtime environments.
		- -
		- -
		- What is SaaS? #flashcard
		  id:: 7424d98c-04e5-447c-8727-ac624dd3c29e
			- With a SaaS model, the applications are completely hosted and managed by the provider. SaaS services take away any need to set up physical infrastructure to host an application. Instead, you simply connect to those applications via the internet and consume the services offered. A majority of SaaS applications today are fully functional via a standard web browser. This also means that there is no requirement to install any client software.
		- -
		- -
		- What is a private cloud? #flashcard
		  id:: ebc89f7a-2828-423c-b71c-7374cc261d2f
			- a private cloud is a cloud deployment model in which your business procures, installs, configures, and manages all the necessary infrastructure and software components in-house. This may sound very similar to traditional on-premises IT. However, the cloud element of it comes from the fact that additional management software is usually deployed to allow different parts of the business to carry out self-service tasks in provisioning compute, storage, network, and software services from an available catalog of services.
			  
			  While public cloud providers offer their services to all businesses across the globe and the services are therefore publicly available, a private cloud is designed solely for your business, where you will not be sharing underlying compute resources with anyone external to your organization.
			  
			  A private cloud is highly customizable to suit the needs of your organization, giving maximum control on key areas such as designing security and infrastructure configuration options. This does not necessarily mean that a private cloud provider (for example, Red Hat OpenStack) is more secure than a public cloud provider. Public cloud providers such as AWS invest vast amounts of money to design security features for the services they offer—features that may be cost-prohibitive if an organization tried to implement them on its own.
		- -
		- -
		- There are three primary models of deployment, listed as follows:
		  id:: c4b23df7-6f39-45f0-9914-afeeddabf62d
		  
		  Public cloud
		  Private cloud
		  Hybrid cloud
		  These models are represented in the following diagram:
		  
		  
		  Figure 1.3 – Cloud deployment models #flashcard
		- -
		- -
		- What is a hybrid cloud? #flashcard
		  id:: e0df2d9d-6e45-4c1c-ac07-578171eedcc1
			- This is a combination of IT services deployed both on-premises (and managed solely by your business) and integrated with one or more third-party cloud providers.
			  
			  Many companies that venture into the public cloud generally start with some form of hybrid model. Often, businesses will move/migrate services to the public cloud to reduce CAPEX investment as they opt for a pay-as-you-go model for the consumption of IT services. An example of this is where companies may need to increase the number of servers deployed for their applications, and rather than procuring more expensive physical hardware, they can set up network connectivity between on-premises infrastructure and the public cloud provider
		- -
	- Chapter 2: Introduction to AWS and the Global Infrastructure
	  collapsed:: true
		- -
		- Amazon Storage Gateway—This enables users to connect their on-premises storage with Amazon S3, offering different gateway options designed to enable offloading of their storage data to Amazon S3. They will continue to have seamless connectivity to that data from their on-premises servers. Depending on the configuration option chosen, Amazon Storage Gateway can maintain a small subnet of frequently accessed data locally, with the bulk of that data in Amazon S3, reducing the total storage hardware needed on premises, which leads to lower capital costs. Alternatively, if on-premises applications are extremely sensitive to network latency, then the Amazon Storage Gateway service can provide data backup capabilities, with the ability to send snapshots of locally stored data to Amazon S3. #flashcard
		  id:: fc59951d-9112-4ed2-8433-6d716549abc1
		- -
	- Chapter 13: Management and Governance on AWS
	  collapsed:: true
		- -
		- What are the 5 categories that **AWS Trusted Advisor** shows? #flashcard
		  id:: bf13c021-3ec2-4b95-965a-ae2096cabe14
			- Cost optimization: Performs checks on your resources to identify which ones are underutilized. AWS Trusted Advisor will then offer recommendations on where you could reduce your costs. For example, Elastic IP addresses are only free if they are attached to a running EC2 instance. AWS charges you an hourly fee for provisioning Elastic IP addresses if they are not being consumed, that is, not attached to any instance, or attached to an instance that is in a stopped state.
			  Performance: Offers recommendations on where you can improve the responsiveness of your applications. For example, if you are using a gp2 EBS volume type for an EC2 instance that seems to be heavily utilized, it can recommend you an upgrade to an io1 EBS volume, which will improve performance.
			  Security: Reports on any resources that have not been configured in accordance with security best practices. For example, if you have not configured MFA on the root account, then AWS will highlight this as a potential security risk and recommend that you configure MFA.
			  Fault tolerance: Identifies options for increasing the resiliency of your AWS solutions. For example, AWS will identify any RDS instance that has not been configured with multi-AZ as a risk factor.
			  Service limits: Checks your AWS account to identify whether you are approaching any service limits or quotas. For example, when using the AWS Auto Scaling service, you have a default limit of configuring up to 200 launch configurations per Region. Should you start to exceed more than 80% of this limit, you will see an alert in Trusted Advisor.
		- -
		- -
		- The difference of cloud computing against just virtualization. #flashcard
		  id:: cf48937d-b0f3-42c8-81c4-7c5540c7d7e0
			- One of the primary characteristics of a cloud computing provider is the ability to provision virtualized infrastructure resources using a self-service management tool. AWS offers such tools in the form of its Management Console (accessible via a web browser), command-line interface (CLI), and direct access to its software application programming interfaces (APIs), to enable customers to provision their resources such as servers, network, storage, and databases. By offering well-defined APIs and enabling automation, cloud providers have made it possible for customers to provision necessary resources using a self-service model. Customers do not have to wait in a queue to get their resources deployed while a cloud engineer performs the necessary configuration for them. Customers can interact with the cloud services directly using API calls, and spin up their own resources in a matter of minutes.
		- -
		- -
		- About cloud implementation models #flashcard
		  id:: cc094fb7-ac3c-46f6-af75-91e52ff43025
			- When it comes to deploying cloud services for your organization, you need to consider which deployment model will suit your business. The decision will be taken based on several factors, such as the industry you are in, compliance and regulatory issues, and also cost management and flexibility of configuration.
			  
			  There are three primary models of deployment, listed as follows:
			  
			  Public cloud
			  Private cloud
			  Hybrid cloud
			  These models are represented in the following diagram:
			  
			  
			  Figure 1.3 – Cloud deployment models
		- -
		- -
		- About AZs and the connections between them #flashcard
		  id:: d36ceab1-bc0b-4162-958f-c4cb3f3e8b25
			- The primary purpose of having multiple AZs is to offer customers the opportunity to build highly available, fault-tolerant, and scalable solutions. This is made possible by the fact that the AZs within a Region are connected to each other over high-bandwidth, low-latency private metro-fiber links, delivering high throughput connections between the zones.
			  
			  An important aspect of this configuration is that you can achieve synchronous replication between AZs. This means that you can deploy multiple copies/replicas of your application on servers across the AZs. If there is an outage at one of the AZs, you can continue to serve your customers from the replica workloads running in the other AZs.
		- -
		- -
		- The ELB not only distributes user traffic to the application servers, but also monitors the health of those servers and sends traffic only if those servers are online and responding #flashcard
		  id:: db61e8fd-ccff-4cba-9e5a-102316860783
		- -
		- -
		- What is the use of edge locations? #flashcard
		  id:: c81b7583-2f16-4d92-b6b6-9b6bbb257ba6
			- most resources that you deploy on AWS are going to be Region-based. For example, an EC2 instance can be deployed in the North Virginia Region, within a specific AZ. Let's assume that the servers host media files and you want to distribute those files to your end users globally. For users based in Sydney, Australia, this would mean pulling these large media files across the public internet directly from the server located in the US, each time they make a request for those files.
			  
			  With edge locations, you can cache frequently accessed files on servers located closer to those users based in Sydney. This means that the time it takes to download those frequently accessed files is drastically reduced, and this improves the UX significantly.
		- -
		- -
		- Which is the *real* use of **S3 Transfer Acceleration**? #flashcard
		  id:: cb727124-712e-44d1-87ae-5b500a008263
			- Edge locations do more than just cache content. For example, Amazon Simple Storage Service (Amazon S3) is an object-storage solution that allows you to create containers (we call them buckets in AWS) in each Region. You can upload any type of data to a bucket and store it. If you need to upload large files to a bucket anywhere in the world, you may experience high latency and lower throughput, as the data needs to traverse the public internet.
			  
			  Amazon S3 Transfer Acceleration is a feature of Amazon S3 that allows you to upload your content to AWS buckets via these edge locations.
		- -
		- -
		- The *true* meaning of **Regional edge caches**. #flashcard
		  id:: 0961dbd7-1442-4ad3-8a32-92a3e17b1405
			- Regional edge caches are highly useful in such situations. There are far fewer regional edge caches than edge locations deployed across the globe, but they are strategically placed. They offer additional storage and cache that will continue to hold the data not accessed frequently for a longer period of time than with standard edge locations.
		- -
		- -
		- About the **AWS Basic Plan** #flashcard
		  id:: 809bed0e-d33b-48d8-85ff-e73eb64b5e59
			- this plan does not come with any real technical support. The Basic support plan is completely free and offers customer support for any account-related issues such as bill payment or if you have issues logging in to your account. You also get access to publicly available documentation, whitepapers, and support forums. You can access the Basic support services via email, chat, and phone 24/7, and the phone support involves getting Amazon to call you on your landline or mobile—so, they pay the call charges.
			  
			  In addition, you also get access to seven basic checks on the Trusted Advisor tool, which helps you to identify best practices for increasing performance and improving security. We will take a look at the Trusted Advisor tool in Chapter 13, Management and Governance on AWS. Finally, you also get alerts regarding interruptions to any AWS services that may impact your deployed resources via the Personal Health Dashboard (PHD)
		- -
		- -
		- About the **AWS Developer Plan** #flashcard
		  id:: 37c1673a-93d5-4c2b-bb03-fe533f1d9335
			- While you get technical support with the Developer support plan, it is limited to generic support primarily around technical configurations with AWS use cases, and the support team will not be able to discuss specific application-layer problems that you might be having. Support is also only available via email (no phone support is offered) during business hours, with access to Cloud Support associates. While you can raise an unlimited number of cases, the case severity and response times are within 24 hours for general guidance and within 12 hours for system-impaired issues.
			  
			  As with the Basic support plan, you only get access to the seven core checks on the AWS Trusted Advisor tool under the Developer support plan.
		- -
		- -
		- About the **AWS Business Plan** #flashcard
		  id:: 90b9c4ba-c9f7-4f94-920f-e659b0a5d90c
			- The Business support plan offers full 24/7 support via email, chat, and telephone. Depending on the severity of the issue, different response times are offered. For example, if you have a production system that is down, you can expect support from a Cloud Support engineer within 1 hour. Also, unlike the Developer support plan, which offers more generic support covering typical AWS use cases, the Business support plan includes helping you troubleshoot interoperability issues between AWS resources and third-party software. The level of support offered is therefore contextual to your use case.
			  
			  For an additional cost, you also get access to AWS Infrastructure Event Management (IEM). This service offers guidance and operational support to help you with your project launch events or migration tasks.
		- -
		- -
		- About **AWS Enterprise Plan** #flashcard
		  id:: 1fd92358-83ad-4918-bcea-7b327f0f3bc2
			- The Enterprise support plan is naturally appropriate for very large organizations, such as multinational companies or companies that have extensively large workloads spread globally.
			  
			  Examples of such companies include Netflix, Amazon Prime, and Dropbox. The Enterprise Support plan stands out because of its different VIP-style offerings such as a designated Technical Account Manager (TAM). Your TAM will actively monitor your environment and work closely with you to actively guide your team through planning, design, and implementation of your cloud projects.
			  
			  Your TAM will assist with optimization tasks and suggest various best-practice methodologies, and also provide access to the best experts within AWS. Another key offering is access to Well-Architected reviews. This allows you to get access to a senior AWS solutions architect who can conduct an audit of your solutions deployed on AWS. AWS will provide guidance and best practices to help you design reliable, scalable, fault-tolerant, and cost-effective solutions.
			  
			  In terms of service-level agreements (SLAs), you get full 24/7 email, chat, and phone support, with access to senior cloud engineers and with a 15-minute response time for business-critical technical issues.
		- -
		- -
			- Here is a table highlighting some key benefits of the different AWS support plans: #flashcard
			  id:: 619f9ea2-f504-44ad-ac2b-9aaad73320b4
				- ![](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/Table_2.1.jpg)
		- -
		- -
		- What is the functionality of the **AWS Service Health Dashboard** (not Personal)?
		  id:: efaee544-b935-4c98-9061-a2925168703b
		  INCLUIR IMAGEN #flashcard
			- AWS publishes service health status across all data centers located in its various Regions. This is the first place you should consider investigating if a service appears to be non-responsive. AWS offers SLAs for its various service offerings
			- ![Figure 2.7 – AWS Service Health Dashboard. Image courtesy of AWS (https://status.aws.amazon.com/)](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_02_07.jpg)
			-
		- -
	- Chapter 4: Identity and Access Management
	  collapsed:: true
		- -
		- What are roles used for? #flashcard
		  id:: 86c263da-ce88-4498-9b80-6fa4aa584bc0
			- IAM roles are generally used to grant access for the following use cases:
			  
			  An AWS service that needs access to another service in your own AWS account, for example, an application running on an EC2 instance that needs access to a database to update customer records.
			  An IAM user in another account that needs access to services in your account via cross-account access.
			  A federated user from another web Identity Provider (Idp) such as Google, Facebook, or Amazon that needs access to resources in your AWS account. IAM roles can be used to grant those external users with only the specific rights to specific services and resources in your account, without the need to create yet another IAM user account for them.
			  A federated corporate user using an identity service such as Microsoft Active Directory, who needs access to a service in your AWS account.
		- -
	- Chapter 5: Amazon Simple Storage Service (S3)
	  collapsed:: true
		- -
		- Define **Block storage** #flashcard
		  id:: 5f71635f-39da-4c7a-90cf-0eb9de4c00c2
			- Block storage is an architectural design that enables the storage of data onto media such as a hard disk, in fixed-sized chunks. Data is broken up into small blocks and placed on the media in these chunks, with a unique address assigned that forms part of its metadata. Block storage makes use of a management software (which can be part of the operating system) to organize the blocks of data. When a user tries to retrieve a file, the management software identifies the blocks to retrieve, reassembles the data, and presents the whole file to the user.
			  
			  On AWS, block storage options are available as Elastic Block Store (EBS). These can be configured as volumes attached to your Elastic Compute Cloud (EC2) instances and offer ultra-low latency required for high-performance workloads. One advantage of EBS volumes is that they are not directly attached to the EC2 instance you deploy, but instead are connected via high-speed network links. This allows you to detach an EBS volume from one EC2 instance and attach it to another if, for example, the first EC2 instance experiences some sort of failure.
		- -
		- -
		- Amazon S3 is one of Amazon's flagship products, and offers a robust, scalable, durable, and cost-effective object storage solution in the cloud. Customers can use Amazon S3 to store any amount of data for a wide range of use cases, including digital media content for websites, data lakes, mobile applications, IoT device data, and big data analytics.
		  id:: 9065c025-0853-40bb-94cc-3904f1071f2e
		  
		  **Amazon S3 can offer up to 99.999999999% durability** and fulfills the storage requirements for a majority of clients and their individual business needs.
		  
		  **What does eleven 9s of durability mean?** According to AWS, if you store 10,000,000 objects on Amazon S3, then on average you can expect to incur a loss of a single object once every 10,000 years. #flashcard
		- -
		- -
		- How can you protect a S3 bucket? #flashcard
		  id:: 1879cbad-f5e7-49b7-b3b8-dd53c1690dd1
			- A bucket policy is applied directly to an entire bucket and can be used to grant access to both the bucket itself and the objects stored within it. Bucket policies can be used to specify different levels of access for different types of objects within the same policy document. A bucket policy document is also written in JavaScript Object Notation Format (JSON) format, just like IAM policies are.
			  
			  With bucket policies, you can also grant anonymous access to object in your buckets, such as a web page, image, or video, which means that anyone with the S3 object URL can access it.
		- -
		- -
		- Infrequent access
		  id:: 79e95a81-9306-4bf0-9979-1266215cc7d9
		  Amazon S3 offers two types of infrequent-access storage classes. These can be used to store objects that you are not going to frequently access, but at the same time, you have instant access to the data when you need it.
		  
		  AWS offers these classes at lower costs on the condition that you do not access your data frequently, as you would with the Standard storage class. To enforce the conditions, AWS will charge additional retrieval fees. Furthermore, there is a minimum object size of 128 kilobytes (KB). You can still store objects under this minimum size, but those objects will be billed as though it is a minimum of 128 KB in size.
		  
		  Amazon S3 Standard-Infrequent Access (S3 Standard-IA)—S3 Standard-IA is designed for data that is just as critical as with the Standard storage class but is infrequently accessed and is therefore ideal for long-term storage, such as for backups, and to act as a data store for DR purposes.
		  
		  Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)—Data stored in this storage class is restricted to one AZ only within the Region you upload it to. This reduces your overall availability of the data to 99.5% but is also much cheaper than the Standard or the Standard-IA storage classes. This also means that if there is an outage of the AZ in which your data is stored, you would have to wait for the AZ to come back online before you can access any data. In the unlikely event of the destruction of an AZ, you may also lose that data.
		  
		  Amazon recommends this class for data that can act as a secondary backup or that can be recreated. #flashcard
		- -
		- -
		- Intelligent-Tiering does not charge a retrieval fee but if objects are archived, retrieval can take some time, depending on the retrieval option chosen. The following table illustrates the retrieval options available:
		  id:: 04459ad3-97ed-474c-b786-62dc0e0dcd9c
		  ![Table 5.1 – Retrieval times for S3 Glacier, Deep Archive, and S3 Intelligent-Tiering archive classes](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/Table_5.1.jpg)
		  Table 5.1 – Retrieval times for S3 Glacier, Deep Archive, and S3 Intelligent-Tiering archive classes #flashcard
		- -
		- -
			- S3 storage class performance and key attributes #flashcard
			  id:: 8cbec442-7347-4e5c-ac2f-03241caf3d57
				- ![](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/Table_5.2_a.jpg)
				- ![Figure 5.4 – S3 storage class performance and key attributes](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/Table_5.2_b.jpg)
				-
		- -
		- -
		- About Snowcone #flashcard
		  id:: abfa0a10-0b43-47a2-bd50-795c97d28581
			- The smallest member of the AWS Snow Family, these devices are the smallest ever and weigh just 4.5 pounds (lb) (2.1 kilograms (kg)). Snowcone devices come with 8 TB of usable storage and are designed for outside use in areas of low network connectivity. Examples include IoT, vehicular, and drone use cases.
			  
			  The device also offers compute capabilities with two vCPUs and 4 GB of memory, as well as USB-C power using a cord and optional battery.
		- -
	- Chapter 6: AWS Networking Services – VPCs, Route53, and CloudFront
	  collapsed:: true
		- -
		- Currently, the largest network on the planet is the internet. Every device that needs to communicate on the internet also requires an IP address. Furthermore, every device on a given network must have a unique IP address. You cannot have two devices in the same network using the same IP address as this would result in a conflict. Given that the four-billion-odd addresses are not sufficient to handle the huge volumes of devices, the Internet Assigned Numbers Authority (IANA) devised a brilliant plan to allocate a range of IP address for private use only. These address ranges are not routable on the internet, which means that businesses (and homes) can configure their internal private networks using these addresses without any possibility of them conflicting with other businesses' networks, particularly if those businesses do not plan to connect their networks together.
		  id:: f59eeb63-375e-490c-9065-6e6f9b18d73e
		  
		  The following IP address ranges are designed for private use:
		  
		  10.0.0.0/8 IP addresses: 10.0.0.0 – 10.255.255.255
		  172.16.0.0/12 IP addresses: 172.16.0.0 – 172.31.255.255
		  192.168.0.0/16 IP addresses: 192.168.0.0 – 192.168.255.255 #flashcard
		- -
		- -
		- In the preceding illustration, we see that businesses can define internal network IP address ranges that are not routable over the internet. These businesses will still require access to the internet, whether to send and receive emails from their customers or host e-commerce applications that their clients would need access to from the internet. To facilitate internet connectivity, public IP addresses are required. However, having to assign each device on the internet with a public IP address would defeat the purpose of private IP ranges and pose a security risk. Instead, the internal network can be configured to access the internet via a service called Network Address Translation (NAT).
		  id:: 42c327a5-f19c-4517-8bd9-eeed13c0b6b2
		  
		  In the following diagram, we can see that businesses are now able to access the internet via a NAT service configured on their external router. The NAT service requires a minimum of one single public IP address and relays requests from the internal devices to the internet, acting as a proxy in between. Replies to those requests are also handled by the NAT service, ensuring that they are correctly redirected to the internal device that made the original request.
		  
		  ![Figure 6.7 – Private IP address ranges used by businesses with internet via NAT services](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_07.jpg)
		  Figure 6.7 – Private IP address ranges used by businesses with internet via NAT services #flashcard
		- -
		- -
		- The way these classes help define network sizes is by splitting the IP address into a network portion and a host portion. Let's look at this individually by class:
		  id:: 910d58c4-adbb-4565-8e9d-b546988877b7
		  
		  Class A – The first 8 bits of a class A address define the network portion, and the remaining 24 bits are used to denote the host portion. Network bits are denoted by 1 (a one in binary) and host bits are denoted by 0 (zeroes). Also, the far-left bit of a class A address is set to 0.
		  Class B – The first 16 bits of a class B address define the network portion, and the remaining 16 bits are used to denote the host portion. In a class B network, the two far-left bits are set to 10.
		  Class C – The first 24 bits of a class C address define the network portion, and the remaining 8 bits are used to denote the host portion. Also, in a class C network, the two far-left bits are set to 11.
		  To better illustrate how these three classes of networks actually look, let's look at the next diagram:
		  
		  ![Figure 6.8 – IP address classes](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_08.jpg)
		  Figure 6.8 – IP address classes #flashcard
		- -
		- -
		- it is important to remember that the first and last IP addresses are unusable. The first IP address is always known as the network ID, which in this case is 192.168.1.0. Here, the last octet would be represented by all zeroes (or, in binary, 00000000). The last IP address is 192.168.1.255, which is known as the broadcast address. Here, the last octet would be represented by all ones (or, in binary, 11111111). #flashcard
		  id:: b0eeb504-e975-4db7-b530-db7ff52f5791
		- -
		- -
		- With AWS Transit Gateway, you can connect your individual VPCs together via the gateway in a hub-and-spoke model. This greatly simplifies your network architecture, as each new VPC that is peered to the gateway needs just a single connection to be able to route traffic to the other VPCs, as long as necessary route table configurations permit it to do so.
		  id:: 1c13244f-06a2-4517-b20b-d5cc295b2840
		  
		  This simplified model is depicted in the following diagram:
		  
		  ![Figure 6.19 – AWS Transit Gateway](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_19.jpg)
		  Figure 6.19 – AWS Transit Gateway #flashcard
		- -
		- -
		- To set up a VPN connection between your on-premises network and the VPC, you need to create a Virtual Private Gateway (VPG) and attach it to your VPC. You will also need to configure a customer gateway, which is a physical or virtual device located in the on-premises network that connects to the VPG over the internet. The setup is illustrated in Figure 6.12. #flashcard
		  id:: 59a3dc1b-560f-4919-8d0e-c44842dee439
		- -
		- -
		- Amazon Route53 offers three primary functions:
		  id:: 1ca36a60-19d2-4b01-81f7-e0b443a0704f
		  
		  Domain registration
		  DNS routing
		  Health checks #flashcard
		- -
		- -
		- Amazon CloudFront is a CDN that helps you to distribute your static and dynamic digital content globally with low-latency connections. AWS CloudFront uses AWS edge locations and regional edge caches to cache content closer to your end users' locations. This means that you can host your content in one specific Region and a user who attempts to access it from another Region will retrieve the content via the edge location over the AWS backbone network. Furthermore, as content is retrieved, it is cached at a local edge location closer to the user for a period (known as a time-to-live or TTL), further improving network latency in subsequent requests for the same content.
		  id:: 9478159e-a166-409c-b499-0f0c04fb3a0e
		  
		  ![Figure 6.21 – A typical CloudFront distribution](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_21.jpg)
		  Figure 6.21 – A typical CloudFront distribution #flashcard
		- -
		- -
		- Without an API gateway, your frontend developer (who builds the frontend user interface) would need to be made aware of all the backend APIs and build the application to call several microservices, to provide complete functionality. Imagine, then, your backend developer later needs to refactor one of the microservices, such as splitting one microservice into two separate microservices, each with its own API. This would result in having to recode some components of the frontend user interface too.
		  id:: 877493e9-7a03-4932-9380-ac3cf3495eec
		  
		  With an API gateway, you essentially create an abstraction layer. This API gateway can be used to expose all the APIs that need to be made available to external clients to call backend services. Requests from those clients can then be routed to the various backend microservices. As per the following diagram, Amazon API Gateway acts as a "front door" for your applications to access backend data, Lambda functions, databases, and more. It handles all the incoming traffic and is capable of processing thousands of concurrent API calls.
		  
		  ![Figure 6.22 – Amazon API Gateway](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_22.jpg)
		  Figure 6.22 – Amazon API Gateway #flashcard
		- -
		-
	- Chapter 7: AWS Compute Services
	  collapsed:: true
		- -
		- A Dedicated Instance is an EC2 instance that is deployed in your VPC on physical hardware that is dedicated to you and not shared with other customers. #flashcard
		  id:: 97f889d4-3f26-4730-9a94-34fbc70be930
		- -
		- -
		- Reserved Pricing Options are not actual EC2 instances that you procure; rather, they are pricing agreements that give you the right to run a specific EC2 configuration, in a specified Region, for a specified duration (1 year to 3 years) at a specific discounted rate. #flashcard
		  id:: 1ad2dafe-53b4-44f6-a370-a70faf38b1fe
		- -
		- -
		- Define Amazon ECR --> Figure 7.7 #flashcard
		  id:: 4202626c-dc4b-4bcb-87d7-187b97d0a3c5
			- Elastic Container Registry (ECR): This is where Docker images are stored on AWS. You can also store your images on Docker Hub or a private registry. Amazon ECR hosts your images in a highly available and high-performance architecture. When the task starts, it reviews the task definition and pulls down the Docker image required from the registry.
		- -
		- -
		- When we say serverless, we do not mean that the compute resource is running without any servers. Ultimately, servers will house the CPU that offers compute capabilities. The term serverless is just used to mean that the customer does not need to manage any actual servers as this falls within the responsibility of AWS.
		  id:: 00951896-52c1-42c4-8e0e-0fb5aabd9d13
		  
		  AWS Lambda is a serverless offering from AWS that allows you to run code and perform some tasks. AWS Lambda is known as a Function as a Service (FaaS) solution that can be used to build an entirely serverless architecture comprised of storage, databases, and network capabilities where you do not manage any underlying servers. #flashcard
		- -
		- -
			- Amazon also offers an alternative solution known as Session Manager, which is a feature of the AWS Systems Manager service offering. Session Manager enables you to manage your EC2 instances and on-premises instances via an interactive browser shell or the AWS CLI tools, without the need to open inbound ports or maintain bastion hosts and SSH keys. It also offers a fully auditable instance management service recording instance access details. #flashcard
			  id:: c7a9c1c3-d6de-483e-9ed2-4ce288355a6e
		- -
		- -
			- Under Availability Zone, select us-east-1a – this is the same zone where we placed Public Subnet One. This way, any frontend web resources in Public Subnet One can access any backend resources in Private Subnet One, allowing those resources to be in the same Availability Zone. #flashcard
			  id:: 45d1616c-9199-4f31-bcf0-bea430227b3e
		- -
	- Chapter 8: AWS Database Services
		- -
			- About relational and non-relational databases #flashcard
			  id:: b3345a26-530b-4e77-a8c9-69dc0c36dc69
				- they have certain restrictions, such as the fact that you need to define the database schema (its structure) before you can add data, and changing this later can be difficult. Non-relational databases offer a lot more flexibility and are used for many modern-day web and mobile applications.
		- -
		- -
			- Let's look at the core components of a DynamoDB database:
			  id:: 3e2bd775-ac5c-4dfc-95fd-ba105d2c5991
			  
			  **Tables**: Like Amazon RDS databases, your data is stored in tables. So, you can have a customers table that will host information about your customers and their orders. Each table will also have a unique primary key, which is crucial for uniquely identifying every record in the table. Records are known as items in DynamoDB Tables.
			-
			- **Items**: Items are like records in Amazon RDS databases. A table can have one or more items, and each item will be a unique combination of attributes that define that item. Items can be up to 400 KB in size and can contain key-value pairs called attributes.
			-
			- **Attributes**: An attribute is like a column heading or a field in an Amazon RDS database. Attributes help define the items in your table. So, in a Customers Table, the attributes could be First-Name or Last-Name and so on. #flashcard
		- -
		- -
			- {{cloze Amazon Neptune}} is a fully managed graph database service and a type of NoSQL database. #flashcard
			  id:: 0d8e8783-86bd-4ec0-a2ad-a17eb9d98a8d
		- -
	- Chapter 9: High Availability and Elasticity on AWS
		- -
			- Explain the *Reliability* pilar of the **Well-Architected Framework** #flashcard
			  id:: 59d764dc-bf12-4188-9999-5a5b28e17ded
				- Reliability
				  Applications deployed in the cloud must be resilient to failures. The resources that your applications depend on (compute, storage, networks, and databases) must be available and reliable. Any technical issues on any of these resources will cause your application to become unreliable and potentially fail.
				  
				  The reliability pillar also focuses on how quickly you can recover from failure based on your architectural design. This is because failures are bound to happen and your architecture must be able to recover from these failures swiftly. One key concept that you should also consider is the fact that replacing a failed component is often better than trying to figure out why the component failed and attempting to resolve the issue that caused the failure. This is because as you spend time trying to troubleshoot the failure, you risk increasing your Recovery Time Objective (RTO). For example, with EC2, you can deploy your application across multiple instances and multiple AZs. You can then configure Elastic Load Balancers and the Auto Scaling service to ensure that if an EC2 instance fails, traffic is routed to only those instances that are healthy, while the failed EC2 instance is replaced automatically in the background.
		- -
		- -
			- Explain the *Performance Efficiency* pillar of the **Well-Architected Framework** #flashcard
			  id:: eb530fac-3810-4faa-837c-9a23e8bb1258
				- Performance efficiency
				  When architecting your cloud solutions, you want to offer the best performance while still ensuring that you are optimized for cost. This means you should always try to select the resource types and sizes based on your performance needs, while monitoring your resources consistently to ensure you maintain those levels of performance in accordance with demand. Performance should not suffer if demand increases. At the same time, you should only provide resources as they are required to avoid underutilization of those resources.
				  
				  You'd often need to incorporate resources that fall across different AWS services, such as compute, storage, and networking, and architecting your solution requires careful planning in addition to configuring each of those resources. For example, if your application is hosted in the London Region, your users in London may experience good performance. However, if you have users in South America, you may experience poor performance due to network latency issues. You can consider using Amazon CloudFront to cache your application content at edge locations closer to your South American users, improving overall application performance.
		- -
		- -
			- Explain the *Security* pillar of the **Well-Architected Framework** #flashcard
			  id:: 700b8b09-d8c7-4da7-9e6e-9c88f83167e0
				- Security
				  You should always keep security in mind whenever you are designing your cloud solutions. You want to ensure that your applications are accessed securely by only authorized users. You also want to ensure data integrity, privacy, and sovereignty. Assigning permissions to users must always be based on the principle of least privilege, ensuring that access is granted only where required to fulfill the job function and nothing more.
				  
				  You should incorporate a backup and disaster recovery strategy for your application solutions, which would also comprise securing the underlying resources that power your application. For example, you must ensure that your databases are backed up or that you regularly create EBS snapshots. Another example is to configure Amazon S3 bucket replication and, if possible, to use cross-regional replication configurations. Finally, you must be able to audit every activity that takes place in your account, and you can use tools such as AWS CloudTrail to maintain an audit log.
		- -
		- -
			- Explain the *Operational Excellence* pillar of the **Well-Architected Framework** #flashcard
			  id:: c6064abb-7780-4902-9e78-648c8e5fdbc6
				- Operational excellence
				  This pillar focuses on achieving operational excellence by making frequent, reversible, and continuous changes to your workloads. Your aim should be to achieve continuous improvements in your processes and procedures. Furthermore, automating operational tasks will strengthen the other pillars, and using Infrastructure as Code (IaC) with tools such as CloudFormation can help to avoid human error and enable consistency in how you respond to events.
				  
				  The operational excellence pillar also suggests anticipating failure and to consider performing fail tests and recovery exercises, from which you can learn how to remove potential sources of failure and mitigate risks. Understanding how your applications fail will also help you design automatic recovery solutions, which will offer consistency and rapid recovery.
		- -
		- -
			- Explain the *Cost Optimization* pillar of the **Well-Architected Framework** #flashcard
			  id:: 8ec8f6af-86a4-49f9-825f-eb5bf4f5ebfb
				- Cost optimization
				  This pillar focuses on ensuring that you architect and build solutions in a manner that avoids unnecessary costs. At the same time, you want to be able to ensure that your applications are highly performant, reliable, operationally efficient, and secure. To achieve cost optimization, you should first understand your spending patterns and analyze where the money is going. Using tools such as Cost Explorer and Cost and Usage Reports will help you with this.
				  
				  Next, you must always try to adopt a consumption model. If you are running development and test servers that only going to be used for 8 hours a day, Monday to Friday, it makes sense to consider procuring those EC2 instances using the On-Demand pricing option. You should then ensure that those servers stopped outside of normal business hours for a potential cost saving of up to 75%
		- -
	- Chapter 14: Implementing Security in AWS
		- -
			- Where possible, AWS always recommends considering opting for managed versions of their products and services rather than adopting a data center mindset management approach. For example, if you require a MySQL database solution, it makes sense to opt for Amazon RDS rather than to provision EC2 instances and deploy the MySQL database software on those instances. #flashcard
			  id:: 0ccde540-2327-4aef-b7fc-51548df8773e
		- -
		- -
			- **AWS GuardDuty** is a threat detection service that can **analyze** and **detect** ==malicious== activity against your AWS **accounts and application workloads**. The service uses various intelligence feeds to be aware of malicious IP addresses and domains. It also uses **machine learning** to help detect anomalies by analyzing data from your CloudTrail event logs, Amazon VPC Flow Logs, and DNS logs. #flashcard
			  id:: 340fccbd-d09a-49cb-8d6f-381c05aa8c40
		- -
		- -
			- What is the function of **AWS Detective**? #flashcard
			  id:: 116663cd-a815-4e2a-84a2-f70bca2901b8
				- Several different AWS services can be used to identify potential security issues, such as the previously discussed Amazon Macie and Amazon GuardDuty. However, if you are trying to determine the root cause of those security findings, you would generally need to process vast amounts of logs and use an Extract, Transform, and Load (ETL) solution to perform the necessary deep-dive analysis required.
				  
				  Amazon Detective can extract time-based events such as logins, network traffic from AWS CloudTrail and Amazon VPC Flow Logs, as well as ingesting your GuardDuty findings. Amazon Detective then helps by producing visualizations using the information that's been ingested, which can help you identify resource behaviors over time and interactions between those resources, ultimately assisting in identifying the root cause of your security issues.
		- -
	- Chapter 15: Billing and Pricing
		- -
			- About data transfers inside or across regions:  #flashcard
			  id:: 16eb96a8-182f-43a5-aa9e-3a93b9ef2ed2
				- **For data transfer within a Region:**
					- If an internet gateway is used to send data to an AWS public service (Amazon S3, DynamoDB, and so on) in the same Region, then there are no data transfer charges.
					  If a NAT gateway is used to access those public services in the same Region, then there is a data processing charge, calculated at a per-GB rate.
					  Data transfers between workloads within the same Availability Zone are free. For certain services, such as EC2, data transfers across Availability Zones will incur a data transfer charge.
				- **For data transfers across Regions**:
					- There is always a data transfer charge.
		- -
		- -
			- About **AWS Cost Explorer** #flashcard
			  id:: 6ccaff4e-dfc7-412c-aaab-941b23b3d77a
				- AWS Cost Explorer enables you to monitor and visualize your costs via dashboards and reports. You can access 12 months of usage and spending data as well as forecasting what your future costs will be for the next 12 months.
		- -
		- -
			- AWS Cost Explorer also provides various recommendations where you can save some money. For example, from the left-hand menu of the AWS Cost Explorer console, you can select Recommendations, under the Reservations category, to see where Cost Explorer suggests purchasing EC2 Reserved Instances (RI) for your existing on-demand workloads as per the following screenshot:
			  id:: 9134183b-42d6-49b5-849d-9617bcb699f4
			  
			  
			  Figure 15.3 – Cost Explorer RI recommendations
			  
			  As you can see, purchasing RI for the two on-demand instances I have running would potentially save me 33% off my final costs. #flashcard
		- -