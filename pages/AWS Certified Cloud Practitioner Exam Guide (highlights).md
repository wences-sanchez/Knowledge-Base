title:: AWS Certified Cloud Practitioner Exam Guide (highlights)
author:: [[]]
full-title:: "AWS Certified Cloud Practitioner Exam Guide"
category:: #books
deck:: [[O'Reilly-Learning::AWS Certified Cloud Practitioner Exam Guide]]

tags:: #[[AWS]] #[[O'Reilly-Learning]]

- #tags #[[AWS]] #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Friday, 23-09-2022]]
	- Chapter 1: What Is Cloud Computing?
		- -
		- What is known as cloud computing? #flashcard
		  id:: 63454583-c2af-42ae-b5b8-75dba4bb635f
			- Cloud computing is a term used to describe the on-demand access to IT services that comprise compute, network, storage, and software services from third-party suppliers, usually via the public internet or some form of direct wide-area network (WAN) access. Companies can provision necessary IT applications for their organization without having to procure and manage their own infrastructure to host those applications. Instead, they lease/rent the required IT infrastructure from such third-party providers.
		- -
		- -
		- What is known as cloud computing? #flashcard
		  id:: 63454583-61cf-456c-94a3-10b4a2cc9c3c
			- Cloud computing is a term used to describe the on-demand access to IT services that comprise compute, network, storage, and software services from third-party suppliers, usually via the public internet or some form of direct wide-area network (WAN) access. Companies can provision necessary IT applications for their organization without having to procure and manage their own infrastructure to host those applications. Instead, they lease/rent the required IT infrastructure from such third-party providers.
			  
			  Cloud computing has existed for many years in some form, since the invention of the internet. In the old days, Hotmail (first launched in 1996 and now branded as Microsoft Outlook) was a prime example of early cloud computing. You could set up email accounts for your colleagues and yourself on Hotmail and use them to communicate. An alternative would be to host your own email servers' (the infrastructure) network connectivity, as well as the email application (the email software). This would ultimately mean additional costs as well as management overheads to maintain the email servers you hosted.
			  
			  Today, cloud computing has become mainstream and is, in several cases, the default option for many companies and start-ups. Currently, Amazon Web Services (AWS) is the largest provider of cloud computing services, offering a variety of cloud IT services in the form of infrastructure, platform, and software solutions.
		- -
		- -
		- ### 6 Advantages of Cloud Computing: #flashcard
		  id:: 63497e85-13ef-4f15-a426-cb2f35db78b3
			- With cloud computing, you pay for the same infrastructure components only as and when you consume them. This on-demand, pay-as-you-go model also means that you save costs when you are not utilizing resources.
			  id:: 63454583-66aa-42e3-ac27-5eac14cbe1fe
			  
			  The shift away from capital expense (CAPEX) for variable expense, also known as operating expense (OPEX), means that you can direct your precious business capital to more important areas of investment, such as developing new products or improving your marketing strategy.
			-
			- Benefit from massive economies of scale:
			-
			- Stop guessing capacity: Traditionally, while carrying out capacity planning, you would procure necessary hardware components for future growth. Predicting future growth is extremely difficult, and this often meant that you would overprovision your environment. The result would be expensive idle resources simply going to waste.
			  id:: 63454583-7794-4e2e-b4f0-32a9e49653d5
			-
			- Increase speed and agility: Cloud vendors such as AWS enable you to launch and configure new IT resources in a few mouse clicks—for example, you can provision a new fleet of servers for your developers within minutes, allowing your organization to exponentially increase its agility in building infrastructure and launching applications
			  id:: 63454583-df8b-4146-a83d-5e633f271113
			-
			- Stop spending money running and maintaining data centers: Hosting your own on-premises infrastructure consumes several hidden costs. In addition to using up precious capital to purchase expensive hardware, you also need a team of engineers to efficiently configure every infrastructure component and lease necessary real estate to rack, stack, and then power up your servers. You would also be required to keep the servers cool with appropriate air-conditioning systems—and that's not all. You would also have to spend money on expensive maintenance contracts to handle the wear and tear of the hardware.
			  id:: 63454583-3097-432d-9a4e-4072ed14519b
			-
			- Go global in minutes: AWS host their data centers in various regions across the globe. Although you may be based in one country, you will have complete access to all regions. This will help you offer lower latency and a superior customer experience, regardless of where your customers are located. Hosting copies of your resources in additional regions can also help you design for disaster recovery (DR) and business continuity requirements.
			  id:: 63454583-1b47-4b49-9c75-c04bb4f64a04
		- -
		- -
		- What is a hypervisor? #flashcard
		  id:: 63454583-da80-439e-950e-5f52a4d861cd
			- A hypervisor is essentially a piece of software that sits between the actual physical hardware and the VMs. It is responsible for enabling the operating systems and applications running on those VMs to access the resources of the physical hardware in a manner that is controlled and that isolates the resources from each other. The hypervisor and its associated management software are used to carve out virtualized representations of the physical hardware components into smaller virtual components, which are then presented as VMs. Each VM can then have its own operating system installed, along with any required applications.
		- -
		- -
		- About virtualization and cloud computing. #flashcard
		  id:: 63454583-1a01-4fcc-8fb4-36a14d72b5c5
			- One of the primary characteristics of a cloud computing provider is the ability to provision virtualized infrastructure resources using a self-service management tool. AWS offers such tools in the form of its Management Console (accessible via a web browser), command-line interface (CLI), and direct access to its software application programming interfaces (APIs), to enable customers to provision their resources such as servers, network, storage, and databases.
		- -
		- -
		- What is PaaS? #flashcard
		  id:: 63454583-66cd-445a-a2c7-bc636cf27030
			- Platform as a Service (PaaS) is another cloud computing model designed to remove the burden of configuring and managing underlying infrastructure resources such as compute, storage, and network services. PaaS is designed to allow your organization to focus on developing your application code and offers you a platform to deploy and manage your application releases, updates, and upgrades.
			  
			  As your developers deploy their application code on the PaaS environment, the provider provisions the infrastructure required to support the application. This will include the necessary network architecture, firewall rules, storage, compute services, operating system management, and runtime environments.
		- -
		- -
		- What is SaaS? #flashcard
		  id:: 63454583-8d69-4faa-8444-9e449d10b7ef
			- With a SaaS model, the applications are completely hosted and managed by the provider. SaaS services take away any need to set up physical infrastructure to host an application. Instead, you simply connect to those applications via the internet and consume the services offered. A majority of SaaS applications today are fully functional via a standard web browser. This also means that there is no requirement to install any client software.
		- -
		- -
		- There are three primary models of deployment, listed as follows:
		  id:: 63497e85-d01d-4b45-bd99-400b11af04e0
		  
		  Public cloud
		  Private cloud
		  Hybrid cloud
		  These models are represented in the following diagram:
		  
		  
		  Figure 1.3 – Cloud deployment models #flashcard
		- -
		- -
		- What is a private cloud? #flashcard
		  id:: 63454583-8a9b-411a-93da-a20754f6cb44
			- a private cloud is a cloud deployment model in which your business procures, installs, configures, and manages all the necessary infrastructure and software components in-house. This may sound very similar to traditional on-premises IT. However, the cloud element of it comes from the fact that additional management software is usually deployed to allow different parts of the business to carry out self-service tasks in provisioning compute, storage, network, and software services from an available catalog of services.
			  
			  While public cloud providers offer their services to all businesses across the globe and the services are therefore publicly available, a private cloud is designed solely for your business, where you will not be sharing underlying compute resources with anyone external to your organization.
			  
			  A private cloud is highly customizable to suit the needs of your organization, giving maximum control on key areas such as designing security and infrastructure configuration options. This does not necessarily mean that a private cloud provider (for example, Red Hat OpenStack) is more secure than a public cloud provider. Public cloud providers such as AWS invest vast amounts of money to design security features for the services they offer—features that may be cost-prohibitive if an organization tried to implement them on its own.
		- -
		- -
		- What is a hybrid cloud? #flashcard
		  id:: 63454583-f9d6-42a4-bad0-1fa1e4811728
			- This is a combination of IT services deployed both on-premises (and managed solely by your business) and integrated with one or more third-party cloud providers.
			  
			  Many companies that venture into the public cloud generally start with some form of hybrid model. Often, businesses will move/migrate services to the public cloud to reduce CAPEX investment as they opt for a pay-as-you-go model for the consumption of IT services. An example of this is where companies may need to increase the number of servers deployed for their applications, and rather than procuring more expensive physical hardware, they can set up network connectivity between on-premises infrastructure and the public cloud provider
		- -