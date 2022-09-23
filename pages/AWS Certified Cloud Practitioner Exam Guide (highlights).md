title:: AWS Certified Cloud Practitioner Exam Guide (highlights)
author:: [[]]
full-title:: "AWS Certified Cloud Practitioner Exam Guide"
category:: #books

tags:: #[[AWS]] #[[O'Reilly-Learning]]

- #tags #[[AWS]] #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Friday, 23-09-2022]]
	- Chapter 1: What Is Cloud Computing?
		- -
		- What is known as cloud computing? #flashcard
			- Cloud computing is a term used to describe the on-demand access to IT services that comprise compute, network, storage, and software services from third-party suppliers, usually via the public internet or some form of direct wide-area network (WAN) access. Companies can provision necessary IT applications for their organization without having to procure and manage their own infrastructure to host those applications. Instead, they lease/rent the required IT infrastructure from such third-party providers.
		- -
		- -
		- What is known as cloud computing? #flashcard
			- Cloud computing is a term used to describe the on-demand access to IT services that comprise compute, network, storage, and software services from third-party suppliers, usually via the public internet or some form of direct wide-area network (WAN) access. Companies can provision necessary IT applications for their organization without having to procure and manage their own infrastructure to host those applications. Instead, they lease/rent the required IT infrastructure from such third-party providers.
			  
			  Cloud computing has existed for many years in some form, since the invention of the internet. In the old days, Hotmail (first launched in 1996 and now branded as Microsoft Outlook) was a prime example of early cloud computing. You could set up email accounts for your colleagues and yourself on Hotmail and use them to communicate. An alternative would be to host your own email servers' (the infrastructure) network connectivity, as well as the email application (the email software). This would ultimately mean additional costs as well as management overheads to maintain the email servers you hosted.
			  
			  Today, cloud computing has become mainstream and is, in several cases, the default option for many companies and start-ups. Currently, Amazon Web Services (AWS) is the largest provider of cloud computing services, offering a variety of cloud IT services in the form of infrastructure, platform, and software solutions.
		- -
		- -
		- 1st advantage of cloud computing #flashcard
			- With cloud computing, you pay for the same infrastructure components only as and when you consume them. This on-demand, pay-as-you-go model also means that you save costs when you are not utilizing resources.
			  
			  The shift away from capital expense (CAPEX) for variable expense, also known as operating expense (OPEX), means that you can direct your precious business capital to more important areas of investment, such as developing new products or improving your marketing strategy.
		- -
		- -
		- 2nd advantage of cloud computing #flashcard
			- Benefit from massive economies of scale:
		- -
		- -
		- 3rd advantage of cloud computing #flashcard
			- Stop guessing capacity: Traditionally, while carrying out capacity planning, you would procure necessary hardware components for future growth. Predicting future growth is extremely difficult, and this often meant that you would overprovision your environment. The result would be expensive idle resources simply going to waste.
		- -
		- -
		- 4th advantage of cloud computing #flashcard
			- Increase speed and agility: Cloud vendors such as AWS enable you to launch and configure new IT resources in a few mouse clicks—for example, you can provision a new fleet of servers for your developers within minutes, allowing your organization to exponentially increase its agility in building infrastructure and launching applications
		- -
		- -
		- 5th advantage of cloud computing #flashcard
			- Stop spending money running and maintaining data centers: Hosting your own on-premises infrastructure consumes several hidden costs. In addition to using up precious capital to purchase expensive hardware, you also need a team of engineers to efficiently configure every infrastructure component and lease necessary real estate to rack, stack, and then power up your servers. You would also be required to keep the servers cool with appropriate air-conditioning systems—and that's not all. You would also have to spend money on expensive maintenance contracts to handle the wear and tear of the hardware.
		- -
		- -
		- 6th advantage of cloud computing #flashcard
			- Go global in minutes: AWS host their data centers in various regions across the globe. Although you may be based in one country, you will have complete access to all regions. This will help you offer lower latency and a superior customer experience, regardless of where your customers are located. Hosting copies of your resources in additional regions can also help you design for disaster recovery (DR) and business continuity requirements.
		- -
		- -
		- What is a hypervisor? #flashcard
			- A hypervisor is essentially a piece of software that sits between the actual physical hardware and the VMs. It is responsible for enabling the operating systems and applications running on those VMs to access the resources of the physical hardware in a manner that is controlled and that isolates the resources from each other. The hypervisor and its associated management software are used to carve out virtualized representations of the physical hardware components into smaller virtual components, which are then presented as VMs. Each VM can then have its own operating system installed, along with any required applications.
		- -
		- -
		- About virtualization and cloud computing. #flashcard
			- One of the primary characteristics of a cloud computing provider is the ability to provision virtualized infrastructure resources using a self-service management tool. AWS offers such tools in the form of its Management Console (accessible via a web browser), command-line interface (CLI), and direct access to its software application programming interfaces (APIs), to enable customers to provision their resources such as servers, network, storage, and databases.
		- -
		- -
		- What is PaaS? #flashcard
			- Platform as a Service (PaaS) is another cloud computing model designed to remove the burden of configuring and managing underlying infrastructure resources such as compute, storage, and network services. PaaS is designed to allow your organization to focus on developing your application code and offers you a platform to deploy and manage your application releases, updates, and upgrades.
			  
			  As your developers deploy their application code on the PaaS environment, the provider provisions the infrastructure required to support the application. This will include the necessary network architecture, firewall rules, storage, compute services, operating system management, and runtime environments.
		- -
		- -
		- What is SaaS? #flashcard
			- With a SaaS model, the applications are completely hosted and managed by the provider. SaaS services take away any need to set up physical infrastructure to host an application. Instead, you simply connect to those applications via the internet and consume the services offered. A majority of SaaS applications today are fully functional via a standard web browser. This also means that there is no requirement to install any client software.
		- -
		- -
		- There are three primary models of deployment, listed as follows:
		  
		  Public cloud
		  Private cloud
		  Hybrid cloud
		  These models are represented in the following diagram:
		  
		  
		  Figure 1.3 – Cloud deployment models #spaced
		- -
		- -
		- What is a private cloud? #flashcard
			- a private cloud is a cloud deployment model in which your business procures, installs, configures, and manages all the necessary infrastructure and software components in-house. This may sound very similar to traditional on-premises IT. However, the cloud element of it comes from the fact that additional management software is usually deployed to allow different parts of the business to carry out self-service tasks in provisioning compute, storage, network, and software services from an available catalog of services.
			  
			  While public cloud providers offer their services to all businesses across the globe and the services are therefore publicly available, a private cloud is designed solely for your business, where you will not be sharing underlying compute resources with anyone external to your organization.
			  
			  A private cloud is highly customizable to suit the needs of your organization, giving maximum control on key areas such as designing security and infrastructure configuration options. This does not necessarily mean that a private cloud provider (for example, Red Hat OpenStack) is more secure than a public cloud provider. Public cloud providers such as AWS invest vast amounts of money to design security features for the services they offer—features that may be cost-prohibitive if an organization tried to implement them on its own.
		- -
		- -
		- What is a hybrid cloud? #flashcard
			- This is a combination of IT services deployed both on-premises (and managed solely by your business) and integrated with one or more third-party cloud providers.
			  
			  Many companies that venture into the public cloud generally start with some form of hybrid model. Often, businesses will move/migrate services to the public cloud to reduce CAPEX investment as they opt for a pay-as-you-go model for the consumption of IT services. An example of this is where companies may need to increase the number of servers deployed for their applications, and rather than procuring more expensive physical hardware, they can set up network connectivity between on-premises infrastructure and the public cloud provider
		- -