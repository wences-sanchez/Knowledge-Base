deck:: [[O'Reilly-Learning::AWS Certified Cloud Practitioner Exam Guide]]

-
- Chapter 1: What Is Cloud Computing?
  collapsed:: true
	- -
	- What is known as cloud computing? #flashcard
	  id:: a21eb884-d3cc-442a-a1f9-c82bf2f962ea
		- Cloud computing is a term used to describe the on-demand access to IT services that comprise compute, network, storage, and software services from third-party suppliers, usually via the public internet or some form of direct wide-area network (WAN) access. Companies can provision necessary IT applications for their organization without having to procure and manage their own infrastructure to host those applications. Instead, they lease/rent the required IT infrastructure from such third-party providers.
	- -
	- -
	- What is known as cloud computing? #flashcard
	  id:: d0b06533-953f-470d-824b-58bdb19289dd
		- Cloud computing is a term used to describe the on-demand access to IT services that comprise compute, network, storage, and software services from third-party suppliers, usually via the public internet or some form of direct wide-area network (WAN) access. Companies can provision necessary IT applications for their organization without having to procure and manage their own infrastructure to host those applications. Instead, they lease/rent the required IT infrastructure from such third-party providers.
		  
		  Cloud computing has existed for many years in some form, since the invention of the internet. In the old days, Hotmail (first launched in 1996 and now branded as Microsoft Outlook) was a prime example of early cloud computing. You could set up email accounts for your colleagues and yourself on Hotmail and use them to communicate. An alternative would be to host your own email servers' (the infrastructure) network connectivity, as well as the email application (the email software). This would ultimately mean additional costs as well as management overheads to maintain the email servers you hosted.
		  
		  Today, cloud computing has become mainstream and is, in several cases, the default option for many companies and start-ups. Currently, Amazon Web Services (AWS) is the largest provider of cloud computing services, offering a variety of cloud IT services in the form of infrastructure, platform, and software solutions.
	- -
	- -
	- 1st advantage of cloud computing #flashcard
	  id:: 367a594b-ec33-4b01-9d9b-2ed6c7ba948f
		- With cloud computing, you pay for the same infrastructure components only as and when you consume them. This on-demand, pay-as-you-go model also means that you save costs when you are not utilizing resources.
		  
		  The shift away from capital expense (CAPEX) for variable expense, also known as operating expense (OPEX), means that you can direct your precious business capital to more important areas of investment, such as developing new products or improving your marketing strategy.
	- -
	- -
	- 2nd advantage of cloud computing #flashcard
	  id:: adafcd56-29ab-43bc-bf51-634a3f7bb2e1
		- Benefit from massive economies of scale:
	- -
	- -
	- 3rd advantage of cloud computing #flashcard
	  id:: 1fd0bf01-27bb-4da1-9d96-feb13e33421b
		- Stop guessing capacity: Traditionally, while carrying out capacity planning, you would procure necessary hardware components for future growth. Predicting future growth is extremely difficult, and this often meant that you would overprovision your environment. The result would be expensive idle resources simply going to waste.
	- -
	- -
	- 4th advantage of cloud computing #flashcard
	  id:: 0a1d4594-8ce2-48a5-ad74-6611d64d7df4
		- Increase speed and agility: Cloud vendors such as AWS enable you to launch and configure new IT resources in a few mouse clicks—for example, you can provision a new fleet of servers for your developers within minutes, allowing your organization to exponentially increase its agility in building infrastructure and launching applications
	- -
	- -
	- 5th advantage of cloud computing #flashcard
	  id:: bda504ad-8c21-457b-a3c8-a92964874d78
		- Stop spending money running and maintaining data centers: Hosting your own on-premises infrastructure consumes several hidden costs. In addition to using up precious capital to purchase expensive hardware, you also need a team of engineers to efficiently configure every infrastructure component and lease necessary real estate to rack, stack, and then power up your servers. You would also be required to keep the servers cool with appropriate air-conditioning systems—and that's not all. You would also have to spend money on expensive maintenance contracts to handle the wear and tear of the hardware.
	- -
	- -
	- 6th advantage of cloud computing #flashcard
	  id:: 7dbc47ee-ac96-42c9-9613-28ec2517119c
		- Go global in minutes: AWS host their data centers in various regions across the globe. Although you may be based in one country, you will have complete access to all regions. This will help you offer lower latency and a superior customer experience, regardless of where your customers are located. Hosting copies of your resources in additional regions can also help you design for disaster recovery (DR) and business continuity requirements.
	- -
	- -
	- What is a hypervisor? #flashcard
	  id:: 693f9179-8dde-4edb-9aee-d202f0f031d0
		- A hypervisor is essentially a piece of software that sits between the actual physical hardware and the VMs. It is responsible for enabling the operating systems and applications running on those VMs to access the resources of the physical hardware in a manner that is controlled and that isolates the resources from each other. The hypervisor and its associated management software are used to carve out virtualized representations of the physical hardware components into smaller virtual components, which are then presented as VMs. Each VM can then have its own operating system installed, along with any required applications.
	- -
	- -
	- About virtualization and cloud computing. #flashcard
	  id:: 80673550-f689-454f-abc6-b83ce2f38063
		- One of the primary characteristics of a cloud computing provider is the ability to provision virtualized infrastructure resources using a self-service management tool. AWS offers such tools in the form of its Management Console (accessible via a web browser), command-line interface (CLI), and direct access to its software application programming interfaces (APIs), to enable customers to provision their resources such as servers, network, storage, and databases.
	- -
	- -
	- What is PaaS? #flashcard
	  id:: 501c82fa-89a9-4454-a400-07b5d4ec0bc1
		- Platform as a Service (PaaS) is another cloud computing model designed to remove the burden of configuring and managing underlying infrastructure resources such as compute, storage, and network services. PaaS is designed to allow your organization to focus on developing your application code and offers you a platform to deploy and manage your application releases, updates, and upgrades.
		  
		  As your developers deploy their application code on the PaaS environment, the provider provisions the infrastructure required to support the application. This will include the necessary network architecture, firewall rules, storage, compute services, operating system management, and runtime environments.
	- -
	- -
	- What is SaaS? #flashcard
	  id:: f99df950-f497-4412-b79e-f5acc4953bd9
		- With a SaaS model, the applications are completely hosted and managed by the provider. SaaS services take away any need to set up physical infrastructure to host an application. Instead, you simply connect to those applications via the internet and consume the services offered. A majority of SaaS applications today are fully functional via a standard web browser. This also means that there is no requirement to install any client software.
	- -
	- -
	- What is a private cloud? #flashcard
	  id:: b900d7e2-3f12-415d-b0f2-0fce1a0b4a74
		- a private cloud is a cloud deployment model in which your business procures, installs, configures, and manages all the necessary infrastructure and software components in-house. This may sound very similar to traditional on-premises IT. However, the cloud element of it comes from the fact that additional management software is usually deployed to allow different parts of the business to carry out self-service tasks in provisioning compute, storage, network, and software services from an available catalog of services.
		  
		  While public cloud providers offer their services to all businesses across the globe and the services are therefore publicly available, a private cloud is designed solely for your business, where you will not be sharing underlying compute resources with anyone external to your organization.
		  
		  A private cloud is highly customizable to suit the needs of your organization, giving maximum control on key areas such as designing security and infrastructure configuration options. This does not necessarily mean that a private cloud provider (for example, Red Hat OpenStack) is more secure than a public cloud provider. Public cloud providers such as AWS invest vast amounts of money to design security features for the services they offer—features that may be cost-prohibitive if an organization tried to implement them on its own.
	- -
	- -
	- There are three primary models of deployment, listed as follows:
	  id:: ade5616f-fa9e-4eab-b858-5ca845178298
	  
	  Public cloud
	  Private cloud
	  Hybrid cloud
	  These models are represented in the following diagram:
	  
	  
	  Figure 1.3 – Cloud deployment models #flashcard
	- -
	- -
	- What is a hybrid cloud? #flashcard
	  id:: b946beef-f9c2-4ddb-9716-e26d62fa9250
		- This is a combination of IT services deployed both on-premises (and managed solely by your business) and integrated with one or more third-party cloud providers.
		  
		  Many companies that venture into the public cloud generally start with some form of hybrid model. Often, businesses will move/migrate services to the public cloud to reduce CAPEX investment as they opt for a pay-as-you-go model for the consumption of IT services. An example of this is where companies may need to increase the number of servers deployed for their applications, and rather than procuring more expensive physical hardware, they can set up network connectivity between on-premises infrastructure and the public cloud provider
	- -
- Chapter 2: Introduction to AWS and the Global Infrastructure
  collapsed:: true
	- -
	- Amazon Storage Gateway—This enables users to connect their on-premises storage with Amazon S3, offering different gateway options designed to enable offloading of their storage data to Amazon S3. They will continue to have seamless connectivity to that data from their on-premises servers. Depending on the configuration option chosen, Amazon Storage Gateway can maintain a small subnet of frequently accessed data locally, with the bulk of that data in Amazon S3, reducing the total storage hardware needed on premises, which leads to lower capital costs. Alternatively, if on-premises applications are extremely sensitive to network latency, then the Amazon Storage Gateway service can provide data backup capabilities, with the ability to send snapshots of locally stored data to Amazon S3. #flashcard
	  id:: 5d803926-19e3-4719-9b90-04de0cba6c71
	- -
- Chapter 13: Management and Governance on AWS
  collapsed:: true
	- -
	- What are the 5 categories that **AWS Trusted Advisor** shows? #flashcard
	  id:: 42c29df3-2820-4eb4-919c-d405084f518a
		- Cost optimization: Performs checks on your resources to identify which ones are underutilized. AWS Trusted Advisor will then offer recommendations on where you could reduce your costs. For example, Elastic IP addresses are only free if they are attached to a running EC2 instance. AWS charges you an hourly fee for provisioning Elastic IP addresses if they are not being consumed, that is, not attached to any instance, or attached to an instance that is in a stopped state.
		  Performance: Offers recommendations on where you can improve the responsiveness of your applications. For example, if you are using a gp2 EBS volume type for an EC2 instance that seems to be heavily utilized, it can recommend you an upgrade to an io1 EBS volume, which will improve performance.
		  Security: Reports on any resources that have not been configured in accordance with security best practices. For example, if you have not configured MFA on the root account, then AWS will highlight this as a potential security risk and recommend that you configure MFA.
		  Fault tolerance: Identifies options for increasing the resiliency of your AWS solutions. For example, AWS will identify any RDS instance that has not been configured with multi-AZ as a risk factor.
		  Service limits: Checks your AWS account to identify whether you are approaching any service limits or quotas. For example, when using the AWS Auto Scaling service, you have a default limit of configuring up to 200 launch configurations per Region. Should you start to exceed more than 80% of this limit, you will see an alert in Trusted Advisor.
	- -
	- -
	- The difference of cloud computing against just virtualization. #flashcard
	  id:: e6bd81bb-b0a6-4a37-9082-c4b5c0a562f1
		- One of the primary characteristics of a cloud computing provider is the ability to provision virtualized infrastructure resources using a self-service management tool. AWS offers such tools in the form of its Management Console (accessible via a web browser), command-line interface (CLI), and direct access to its software application programming interfaces (APIs), to enable customers to provision their resources such as servers, network, storage, and databases. By offering well-defined APIs and enabling automation, cloud providers have made it possible for customers to provision necessary resources using a self-service model. Customers do not have to wait in a queue to get their resources deployed while a cloud engineer performs the necessary configuration for them. Customers can interact with the cloud services directly using API calls, and spin up their own resources in a matter of minutes.
	- -
	- -
	- About cloud implementation models #flashcard
	  id:: a105357b-e09a-456b-93d5-278e5742b71b
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
	  id:: 716e2b8b-8572-402f-974d-37cce527f04f
		- The primary purpose of having multiple AZs is to offer customers the opportunity to build highly available, fault-tolerant, and scalable solutions. This is made possible by the fact that the AZs within a Region are connected to each other over high-bandwidth, low-latency private metro-fiber links, delivering high throughput connections between the zones.
		  
		  An important aspect of this configuration is that you can achieve synchronous replication between AZs. This means that you can deploy multiple copies/replicas of your application on servers across the AZs. If there is an outage at one of the AZs, you can continue to serve your customers from the replica workloads running in the other AZs.
	- -
	- -
	- The ELB not only distributes user traffic to the application servers, but also monitors the health of those servers and sends traffic only if those servers are online and responding #flashcard
	  id:: 10eee881-2ffb-4b46-abd0-1fac369eab5b
	- -
	- -
	- What is the use of edge locations? #flashcard
	  id:: 03d2ed56-5683-4d9d-9d40-f44dc5c58a27
		- most resources that you deploy on AWS are going to be Region-based. For example, an EC2 instance can be deployed in the North Virginia Region, within a specific AZ. Let's assume that the servers host media files and you want to distribute those files to your end users globally. For users based in Sydney, Australia, this would mean pulling these large media files across the public internet directly from the server located in the US, each time they make a request for those files.
		  
		  With edge locations, you can cache frequently accessed files on servers located closer to those users based in Sydney. This means that the time it takes to download those frequently accessed files is drastically reduced, and this improves the UX significantly.
	- -
	- -
	- Which is the *real* use of **S3 Transfer Acceleration**? #flashcard
	  id:: d63f42c2-db7a-4316-9430-bb6b28e90ee7
		- Edge locations do more than just cache content. For example, Amazon Simple Storage Service (Amazon S3) is an object-storage solution that allows you to create containers (we call them buckets in AWS) in each Region. You can upload any type of data to a bucket and store it. If you need to upload large files to a bucket anywhere in the world, you may experience high latency and lower throughput, as the data needs to traverse the public internet.
		  
		  Amazon S3 Transfer Acceleration is a feature of Amazon S3 that allows you to upload your content to AWS buckets via these edge locations.
	- -
	- -
	- The *true* meaning of **Regional edge caches**. #flashcard
	  id:: b383262d-dd7b-4e15-b1f4-00b38ca25313
		- Regional edge caches are highly useful in such situations. There are far fewer regional edge caches than edge locations deployed across the globe, but they are strategically placed. They offer additional storage and cache that will continue to hold the data not accessed frequently for a longer period of time than with standard edge locations.
	- -
	- -
	- About the **AWS Basic Plan** #flashcard
	  id:: 3e4d3689-9a8e-46a8-8b1d-74d7f6fba2f4
		- this plan does not come with any real technical support. The Basic support plan is completely free and offers customer support for any account-related issues such as bill payment or if you have issues logging in to your account. You also get access to publicly available documentation, whitepapers, and support forums. You can access the Basic support services via email, chat, and phone 24/7, and the phone support involves getting Amazon to call you on your landline or mobile—so, they pay the call charges.
		  
		  In addition, you also get access to seven basic checks on the Trusted Advisor tool, which helps you to identify best practices for increasing performance and improving security. We will take a look at the Trusted Advisor tool in Chapter 13, Management and Governance on AWS. Finally, you also get alerts regarding interruptions to any AWS services that may impact your deployed resources via the Personal Health Dashboard (PHD)
	- -
	- -
	- About the **AWS Developer Plan** #flashcard
	  id:: b23891eb-cf88-45a4-9aaa-f558ef2205a4
		- While you get technical support with the Developer support plan, it is limited to generic support primarily around technical configurations with AWS use cases, and the support team will not be able to discuss specific application-layer problems that you might be having. Support is also only available via email (no phone support is offered) during business hours, with access to Cloud Support associates. While you can raise an unlimited number of cases, the case severity and response times are within 24 hours for general guidance and within 12 hours for system-impaired issues.
		  
		  As with the Basic support plan, you only get access to the seven core checks on the AWS Trusted Advisor tool under the Developer support plan.
	- -
	- -
	- About the **AWS Business Plan** #flashcard
	  id:: 91849370-7ee3-459e-aac1-1d6a886bc054
		- The Business support plan offers full 24/7 support via email, chat, and telephone. Depending on the severity of the issue, different response times are offered. For example, if you have a production system that is down, you can expect support from a Cloud Support engineer within 1 hour. Also, unlike the Developer support plan, which offers more generic support covering typical AWS use cases, the Business support plan includes helping you troubleshoot interoperability issues between AWS resources and third-party software. The level of support offered is therefore contextual to your use case.
		  
		  For an additional cost, you also get access to AWS Infrastructure Event Management (IEM). This service offers guidance and operational support to help you with your project launch events or migration tasks.
	- -
	- -
	- About **AWS Enterprise Plan** #flashcard
	  id:: dfb12bf4-ca39-4b88-84aa-3d1caa8a6361
		- The Enterprise support plan is naturally appropriate for very large organizations, such as multinational companies or companies that have extensively large workloads spread globally.
		  
		  Examples of such companies include Netflix, Amazon Prime, and Dropbox. The Enterprise Support plan stands out because of its different VIP-style offerings such as a designated Technical Account Manager (TAM). Your TAM will actively monitor your environment and work closely with you to actively guide your team through planning, design, and implementation of your cloud projects.
		  
		  Your TAM will assist with optimization tasks and suggest various best-practice methodologies, and also provide access to the best experts within AWS. Another key offering is access to Well-Architected reviews. This allows you to get access to a senior AWS solutions architect who can conduct an audit of your solutions deployed on AWS. AWS will provide guidance and best practices to help you design reliable, scalable, fault-tolerant, and cost-effective solutions.
		  
		  In terms of service-level agreements (SLAs), you get full 24/7 email, chat, and phone support, with access to senior cloud engineers and with a 15-minute response time for business-critical technical issues.
	- -
	- -
		- Here is a table highlighting some key benefits of the different AWS support plans: #flashcard
		  id:: 6b83e5f2-8d71-4c81-a796-a29411ee30aa
			- ![](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/Table_2.1.jpg)
	- -
	- -
	- What is the functionality of the **AWS Service Health Dashboard** (not Personal)?
	  id:: d3219464-7dc1-47d8-b128-508a4783551f
	  INCLUIR IMAGEN #flashcard
		- AWS publishes service health status across all data centers located in its various Regions. This is the first place you should consider investigating if a service appears to be non-responsive. AWS offers SLAs for its various service offerings
		- ![Figure 2.7 – AWS Service Health Dashboard. Image courtesy of AWS (https://status.aws.amazon.com/)](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_02_07.jpg)
		-
	- -
- Chapter 4: Identity and Access Management
  collapsed:: true
	- -
	- What are roles used for? #flashcard
	  id:: 95935a00-1365-4f0a-9a1d-dda034ccd1ad
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
	  id:: 5c5f4305-2eec-4695-8fcb-8ed70079da6a
		- Block storage is an architectural design that enables the storage of data onto media such as a hard disk, in fixed-sized chunks. Data is broken up into small blocks and placed on the media in these chunks, with a unique address assigned that forms part of its metadata. Block storage makes use of a management software (which can be part of the operating system) to organize the blocks of data. When a user tries to retrieve a file, the management software identifies the blocks to retrieve, reassembles the data, and presents the whole file to the user.
		  
		  On AWS, block storage options are available as Elastic Block Store (EBS). These can be configured as volumes attached to your Elastic Compute Cloud (EC2) instances and offer ultra-low latency required for high-performance workloads. One advantage of EBS volumes is that they are not directly attached to the EC2 instance you deploy, but instead are connected via high-speed network links. This allows you to detach an EBS volume from one EC2 instance and attach it to another if, for example, the first EC2 instance experiences some sort of failure.
	- -
	- -
	- Amazon S3 is one of Amazon's flagship products, and offers a robust, scalable, durable, and cost-effective object storage solution in the cloud. Customers can use Amazon S3 to store any amount of data for a wide range of use cases, including digital media content for websites, data lakes, mobile applications, IoT device data, and big data analytics.
	  id:: 1fda84a1-8d54-4f3b-8194-9e9e910d747e
	  
	  **Amazon S3 can offer up to 99.999999999% durability** and fulfills the storage requirements for a majority of clients and their individual business needs.
	  
	  **What does eleven 9s of durability mean?** According to AWS, if you store 10,000,000 objects on Amazon S3, then on average you can expect to incur a loss of a single object once every 10,000 years. #flashcard
	- -
	- -
	- How can you protect a S3 bucket? #flashcard
	  id:: 1519327c-f154-4599-a9ad-5c5589ba03eb
		- A bucket policy is applied directly to an entire bucket and can be used to grant access to both the bucket itself and the objects stored within it. Bucket policies can be used to specify different levels of access for different types of objects within the same policy document. A bucket policy document is also written in JavaScript Object Notation Format (JSON) format, just like IAM policies are.
		  
		  With bucket policies, you can also grant anonymous access to object in your buckets, such as a web page, image, or video, which means that anyone with the S3 object URL can access it.
	- -
	- -
	- Infrequent access
	  id:: 153cc25b-b135-4e74-9d50-b3c633424b8b
	  Amazon S3 offers two types of infrequent-access storage classes. These can be used to store objects that you are not going to frequently access, but at the same time, you have instant access to the data when you need it.
	  
	  AWS offers these classes at lower costs on the condition that you do not access your data frequently, as you would with the Standard storage class. To enforce the conditions, AWS will charge additional retrieval fees. Furthermore, there is a minimum object size of 128 kilobytes (KB). You can still store objects under this minimum size, but those objects will be billed as though it is a minimum of 128 KB in size.
	  
	  Amazon S3 Standard-Infrequent Access (S3 Standard-IA)—S3 Standard-IA is designed for data that is just as critical as with the Standard storage class but is infrequently accessed and is therefore ideal for long-term storage, such as for backups, and to act as a data store for DR purposes.
	  
	  Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)—Data stored in this storage class is restricted to one AZ only within the Region you upload it to. This reduces your overall availability of the data to 99.5% but is also much cheaper than the Standard or the Standard-IA storage classes. This also means that if there is an outage of the AZ in which your data is stored, you would have to wait for the AZ to come back online before you can access any data. In the unlikely event of the destruction of an AZ, you may also lose that data.
	  
	  Amazon recommends this class for data that can act as a secondary backup or that can be recreated. #flashcard
	- -
	- -
	- Intelligent-Tiering does not charge a retrieval fee but if objects are archived, retrieval can take some time, depending on the retrieval option chosen. The following table illustrates the retrieval options available:
	  id:: 710bbfe2-563c-43de-945a-b6b79a16876a
	  ![Table 5.1 – Retrieval times for S3 Glacier, Deep Archive, and S3 Intelligent-Tiering archive classes](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/Table_5.1.jpg)
	  Table 5.1 – Retrieval times for S3 Glacier, Deep Archive, and S3 Intelligent-Tiering archive classes #flashcard
	- -
	- -
		- S3 storage class performance and key attributes #flashcard
		  id:: 21f1e660-4674-422d-83af-f7a2585caced
			- ![](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/Table_5.2_a.jpg)
			- ![Figure 5.4 – S3 storage class performance and key attributes](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/Table_5.2_b.jpg)
			-
	- -
	- -
	- About Snowcone #flashcard
	  id:: 278e63b5-520b-4f08-adc1-af811b1154e2
		- The smallest member of the AWS Snow Family, these devices are the smallest ever and weigh just 4.5 pounds (lb) (2.1 kilograms (kg)). Snowcone devices come with 8 TB of usable storage and are designed for outside use in areas of low network connectivity. Examples include IoT, vehicular, and drone use cases.
		  
		  The device also offers compute capabilities with two vCPUs and 4 GB of memory, as well as USB-C power using a cord and optional battery.
	- -
- Chapter 6: AWS Networking Services – VPCs, Route53, and CloudFront
  collapsed:: true
	- -
	- Currently, the largest network on the planet is the internet. Every device that needs to communicate on the internet also requires an IP address. Furthermore, every device on a given network must have a unique IP address. You cannot have two devices in the same network using the same IP address as this would result in a conflict. Given that the four-billion-odd addresses are not sufficient to handle the huge volumes of devices, the Internet Assigned Numbers Authority (IANA) devised a brilliant plan to allocate a range of IP address for private use only. These address ranges are not routable on the internet, which means that businesses (and homes) can configure their internal private networks using these addresses without any possibility of them conflicting with other businesses' networks, particularly if those businesses do not plan to connect their networks together.
	  id:: 4b6ae107-2390-4223-b779-9d48dd3b2538
	  
	  The following IP address ranges are designed for private use:
	  
	  10.0.0.0/8 IP addresses: 10.0.0.0 – 10.255.255.255
	  172.16.0.0/12 IP addresses: 172.16.0.0 – 172.31.255.255
	  192.168.0.0/16 IP addresses: 192.168.0.0 – 192.168.255.255 #flashcard
	- -
	- -
	- In the preceding illustration, we see that businesses can define internal network IP address ranges that are not routable over the internet. These businesses will still require access to the internet, whether to send and receive emails from their customers or host e-commerce applications that their clients would need access to from the internet. To facilitate internet connectivity, public IP addresses are required. However, having to assign each device on the internet with a public IP address would defeat the purpose of private IP ranges and pose a security risk. Instead, the internal network can be configured to access the internet via a service called Network Address Translation (NAT).
	  id:: f3adc83c-1361-43c9-85e0-9fa1c3fae57d
	  
	  In the following diagram, we can see that businesses are now able to access the internet via a NAT service configured on their external router. The NAT service requires a minimum of one single public IP address and relays requests from the internal devices to the internet, acting as a proxy in between. Replies to those requests are also handled by the NAT service, ensuring that they are correctly redirected to the internal device that made the original request.
	  
	  ![Figure 6.7 – Private IP address ranges used by businesses with internet via NAT services](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_07.jpg)
	  Figure 6.7 – Private IP address ranges used by businesses with internet via NAT services #flashcard
	- -
	- -
	- The way these classes help define network sizes is by splitting the IP address into a network portion and a host portion. Let's look at this individually by class:
	  id:: c0c36679-7a36-4dc7-bcc1-5c382eea39c3
	  
	  Class A – The first 8 bits of a class A address define the network portion, and the remaining 24 bits are used to denote the host portion. Network bits are denoted by 1 (a one in binary) and host bits are denoted by 0 (zeroes). Also, the far-left bit of a class A address is set to 0.
	  Class B – The first 16 bits of a class B address define the network portion, and the remaining 16 bits are used to denote the host portion. In a class B network, the two far-left bits are set to 10.
	  Class C – The first 24 bits of a class C address define the network portion, and the remaining 8 bits are used to denote the host portion. Also, in a class C network, the two far-left bits are set to 11.
	  To better illustrate how these three classes of networks actually look, let's look at the next diagram:
	  
	  ![Figure 6.8 – IP address classes](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_08.jpg)
	  Figure 6.8 – IP address classes #flashcard
	- -
	- -
	- it is important to remember that the first and last IP addresses are unusable. The first IP address is always known as the network ID, which in this case is 192.168.1.0. Here, the last octet would be represented by all zeroes (or, in binary, 00000000). The last IP address is 192.168.1.255, which is known as the broadcast address. Here, the last octet would be represented by all ones (or, in binary, 11111111). #flashcard
	  id:: cdd092d3-aba1-446f-bd3a-1f26d2c51f67
	- -
	- -
	- With AWS Transit Gateway, you can connect your individual VPCs together via the gateway in a hub-and-spoke model. This greatly simplifies your network architecture, as each new VPC that is peered to the gateway needs just a single connection to be able to route traffic to the other VPCs, as long as necessary route table configurations permit it to do so.
	  id:: 8906e4d2-8e94-418b-ba87-1278555f3454
	  
	  This simplified model is depicted in the following diagram:
	  
	  ![Figure 6.19 – AWS Transit Gateway](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_19.jpg)
	  Figure 6.19 – AWS Transit Gateway #flashcard
	- -
	- -
	- To set up a VPN connection between your on-premises network and the VPC, you need to create a Virtual Private Gateway (VPG) and attach it to your VPC. You will also need to configure a customer gateway, which is a physical or virtual device located in the on-premises network that connects to the VPG over the internet. The setup is illustrated in Figure 6.12. #flashcard
	  id:: 3584f86b-08c8-441a-afc5-b183a28f6356
	- -
	- -
	- Amazon Route53 offers three primary functions:
	  id:: b4ceaf42-3031-46ed-b7a7-aaf0d8d93e38
	  
	  Domain registration
	  DNS routing
	  Health checks #flashcard
	- -
	- -
	- Amazon CloudFront is a CDN that helps you to distribute your static and dynamic digital content globally with low-latency connections. AWS CloudFront uses AWS edge locations and regional edge caches to cache content closer to your end users' locations. This means that you can host your content in one specific Region and a user who attempts to access it from another Region will retrieve the content via the edge location over the AWS backbone network. Furthermore, as content is retrieved, it is cached at a local edge location closer to the user for a period (known as a time-to-live or TTL), further improving network latency in subsequent requests for the same content.
	  id:: ccf704fa-2f50-4390-8af8-be14d4a08ef3
	  
	  ![Figure 6.21 – A typical CloudFront distribution](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_21.jpg)
	  Figure 6.21 – A typical CloudFront distribution #flashcard
	- -
	- -
	- Without an API gateway, your frontend developer (who builds the frontend user interface) would need to be made aware of all the backend APIs and build the application to call several microservices, to provide complete functionality. Imagine, then, your backend developer later needs to refactor one of the microservices, such as splitting one microservice into two separate microservices, each with its own API. This would result in having to recode some components of the frontend user interface too.
	  id:: c35be7f9-af1e-4db9-9b74-571afe5bdaa8
	  
	  With an API gateway, you essentially create an abstraction layer. This API gateway can be used to expose all the APIs that need to be made available to external clients to call backend services. Requests from those clients can then be routed to the various backend microservices. As per the following diagram, Amazon API Gateway acts as a "front door" for your applications to access backend data, Lambda functions, databases, and more. It handles all the incoming traffic and is capable of processing thousands of concurrent API calls.
	  
	  ![Figure 6.22 – Amazon API Gateway](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781801075930/files/image/B17124_06_22.jpg)
	  Figure 6.22 – Amazon API Gateway #flashcard
	- -
	-
- Chapter 7: AWS Compute Services
	- -
	- A Dedicated Instance is an EC2 instance that is deployed in your VPC on physical hardware that is dedicated to you and not shared with other customers. #flashcard
	  id:: 5d7075f9-adb4-404e-a236-d9e9b5dcf509
	- -
	- -
	- Reserved Pricing Options are not actual EC2 instances that you procure; rather, they are pricing agreements that give you the right to run a specific EC2 configuration, in a specified Region, for a specified duration (1 year to 3 years) at a specific discounted rate. #flashcard
	  id:: 351b7d20-3806-49ea-897f-28f8143c6dbe
	- -
	- -
	- Define Amazon ECR --> Figure 7.7 #flashcard
	  id:: 867d4605-c63e-4c52-aec4-303ec3d67e50
		- Elastic Container Registry (ECR): This is where Docker images are stored on AWS. You can also store your images on Docker Hub or a private registry. Amazon ECR hosts your images in a highly available and high-performance architecture. When the task starts, it reviews the task definition and pulls down the Docker image required from the registry.
	- -
	- -
	- When we say serverless, we do not mean that the compute resource is running without any servers. Ultimately, servers will house the CPU that offers compute capabilities. The term serverless is just used to mean that the customer does not need to manage any actual servers as this falls within the responsibility of AWS.
	  id:: 4dd738f3-cdc1-48bb-8042-2efbed2a089b
	  
	  AWS Lambda is a serverless offering from AWS that allows you to run code and perform some tasks. AWS Lambda is known as a Function as a Service (FaaS) solution that can be used to build an entirely serverless architecture comprised of storage, databases, and network capabilities where you do not manage any underlying servers. #flashcard
	- -
	- -
		- Amazon also offers an alternative solution known as Session Manager, which is a feature of the AWS Systems Manager service offering. Session Manager enables you to manage your EC2 instances and on-premises instances via an interactive browser shell or the AWS CLI tools, without the need to open inbound ports or maintain bastion hosts and SSH keys. It also offers a fully auditable instance management service recording instance access details. #flashcard
		  id:: cee0f3cf-37f9-44a0-94ca-36bedd4d2b8b
	- -
	- -
		- Under Availability Zone, select us-east-1a – this is the same zone where we placed Public Subnet One. This way, any frontend web resources in Public Subnet One can access any backend resources in Private Subnet One, allowing those resources to be in the same Availability Zone. #flashcard
	- -