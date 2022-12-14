title:: Exam Ref AZ-900 Microsoft Azure Fundamentals (highlights)
deck:: [[O'Reilly-Learning::Exam Ref AZ-900 Microsoft Azure Fundamentals]]
author:: [[Jim Cheshire]]
full-title:: "Exam Ref AZ-900 Microsoft Azure Fundamentals"
category:: #books

tags:: Azure O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Wednesday, 14-12-2022]]
	- Skill 1.2: Describe the benefit of using cloud services
		- -
			- VMs make it easy to add additional computers when necessary, and they allow you to better manage computer resources such as CPU, disk space, and memory. For that reason, VMs are commonplace in most businesses. #flashcard
			  id:: cad439fb-fd35-4b12-bd30-6dcc35c13ba3
		- -
	- Chapter summary
		- -
			- What does *tenant* mean (in Azure)? #flashcard
			  id:: 6c4dca94-e56a-4351-8c81-deac263d8e2d
				- The public cloud model is sometimes referred to as a multitenant environment. Multiple companies and users share the same infrastructure. VMs and other infrastructure are allocated to users as they need them, and when they no longer need them, they are returned to the pool to be used by other users. The network is available publicly over the internet, but you do have the ability to put security methods in place to control access to your resources.
				  
				  The private cloud model is sometimes referred to as a single-tenant environment. All infrastructure is private to an individual or a company, and the network is only available within the private cloud itself. It is not exposed to the internet. In many cases, the infrastructure used in a private cloud is owned by the company, but not always. It’s possible to host a private cloud in a third-party data center.
		- -
	- Skill 2.1: Describe the core architectural components of Azure
		- -
			- Availability zones aren’t available in all Azure regions, nor are they available for all Azure services in regions that support them. For the most up-to-date list of availability zone-enabled regions and services, see https://bit.ly/az900-azones. #flashcard
			  id:: bb799137-f441-41d5-8c5d-a2269add874a
		- -
		- -
			- Customers only see Regions
			  id:: b2078496-cf9f-4f0c-82e1-ffc483c39a9c
			  
			  When a customer is creating Azure resources, only the region is visible. The concept of geographies is an internal implementation of Azure that customers don’t really have visibility of when using Azure. Customers also don’t have visibility into the concept of regional pairs, but they can see each region within a regional pair. #flashcard
		- -
	- Skill 2.2: Describe Azure compute and networking services
		- -
			- When to use AKS in Azure #flashcard
			  id:: 4bb84d89-43e7-4b23-8add-50162782dd9b
				- ACI is designed to work with simple applications. You can define a container group and run multiple containers within an ACI instance, but ACI isn’t a good choice for you if you have an application that is used heavily by many people and that might need to take advantage of scaling. Instead, Azure Kubernetes Service (AKS) would be a better choice.
		- -
		- -
			- The new VM is a guest on a physical computer in an Azure datacenter. In that datacenter is a physical rack of computer servers, and our VM is hosted on one of those servers. The host computer is managed by Microsoft, but you manage the VM because this is an IaaS offering in Azure. #flashcard
			  id:: 315b6942-0c9d-4034-aabd-5d09a8b18c96
		- -
		- -
			- Explain what *planned maintenance* is in Azure #flashcard
			  id:: 482fb356-ace9-4dfe-84b4-49c77ccd8327
				- Planned maintenance refers to planned updates that Microsoft makes to the host computer. This includes things like operating system updates, driver updates, and so on. In many cases, updates won’t affect your VM, but if Microsoft installs an update that requires a reboot of the host computer, your VM will be down during that reboot.
		- -
		- -
			- Explain what *unplanned maintenance* is in Azure #flashcard
			  id:: f16fb77d-3ebc-4a5c-bdbc-609d971540dd
				- Azure has underlying systems that constantly monitor the health of computer components. If one of these underlying systems detects that a component within the host computer might fail soon, Azure will flag the computer for unplanned maintenance. In an unplanned maintenance event, Azure will attempt to move your VM to a healthy host computer. When it does this, it preserves the state of the VM, including what’s in memory and any files that are open. It only takes Azure a short time to move the VM, during which time it’s in a paused state. In a case where the move operation fails, the VM will experience unexpected downtime.
		- -
		- -
			- Azure offers another feature for VMs called scale sets that solves these problems nicely. When you create a scale set, you tell Azure what operating system you want to run and then you tell Azure how many VMs you want in your scale set. You have many other options such as creating a load balancer or gateway and so forth. Azure will create as many VMs as you specify (up to 1,000) in one easy step. #flashcard
		- -
		- -
			- This diagram is simplified, but it illustrates the basics of how App Service works. Azure Load Balancer distributes traffic to a special VM within App Service called a front end. The front end is running special software that allows it to effectively distribute traffic to the VMs that are actually running your web app. These VMs run inside of an App Service plan, a logical container for one or more VMs that are running your web app.
			  id:: 0c29c1cb-b028-4be8-9ee8-ee446a5f046a
			  
			  
			  FIGURE 2-20 A high-level representation of Azure App Service #flashcard
		- -
		- -
			- Every web app you create in App Service runs inside of an App Service plan. An App Service plan is created within a specific Azure region, and it specifies how many VMs your app runs on and the properties of those VMs. #flashcard
			  id:: 2e1696ab-58d6-49a9-8504-b7333d60cdfc
		- -
		- -
			- You are charged for App Service plans even when no web apps are running in them. If you do have web apps in your App Service plan, you are still charged if you stop the web apps. The only way to avoid being billed for an App Service plan is to delete it. #flashcard
			  id:: 4dfa39fd-38de-48a7-910e-725d926c6507
		- -
		- -
			- About the importance of Kubernetes in job offers #flashcard
			  id:: 49880f9b-1c4d-4979-9e81-9332fd4507a3
				- While AKS makes adopting and managing Kubernetes easier, it doesn’t completely obfuscate Kubernetes. To deploy your applications, you still need to understand how to use Kubernetes, and in some cases, you’ll need to use the Kubernetes command line. Azure, however, makes it far easier than doing all the legwork and maintenance yourself
		- -
		- -
			- Explain what is a *site-to-site connection*. #flashcard
			  id:: aaa5ae9b-ac41-4b5a-b5f7-d4dbdff08726
				- A site-to-site connection allows you to connect your VNet to an on-premises network using an encrypted VPN connection. Site-to-site connections require you to configure a VPN device on your on-premises network, and that VPN device must have a public-facing IP address. Network traffic between your VNet and your on-premises network travels over an encrypted VPN connection.
		- -
		- -
			- Explain what is a *point-to-site connection*. #flashcard
			  id:: e82b708d-dacb-4f72-97da-863b36009e76
				- A point-to-site connection connects your VNet to a single device. That device can be a computer, but it can also be a mobile device, such as a tablet or a smartphone. When using a point-to-site connection, software on the device establishes a VPN connection to VPN Gateway, and all traffic is encrypted and travels over that connection.
		- -
	- Skill 2.3: Describe Azure Storage services
		- -
			- There are two redundancy options designed to replicate your data only in the primary region. They are locally redundant storage (LRS) and zone-redundant storage (ZRS). When using LRS, Azure makes three copies of your data within a single datacenter. ZRS also makes three copies of your data, but each copy is in a separate availability zone in a separate datacenter. #flashcard
			  id:: 2ad7be49-4f96-4c64-b044-93fa88393a07
		- -
		- -
			- When you use ZRS, each copy of your data is in a separate datacenter because Azure uses availability zones for redundancy. ZRS has the added benefit of protecting your data from a problem impacting a single datacenter, but it won’t protect you from a large-scale disaster in an Azure region. #flashcard
			  id:: c6f3708d-07eb-4baf-a08b-a26daae069bd
		- -
		- -
			- Azure can also distribute copies of your data across Azure regions. These options protect you from a large-scale impact in a particular Azure region. Just as with primary-region redundancy, there are two redundancy options for multiple-region redundancy. They are geo-redundant storage (GRS) and geo-zone-redundant storage (GZRS).
			  id:: f0c492c1-1251-4b4e-a2e4-16e3df892ea2
			  
			  GRS creates three copies of your data in the primary region using LRS. It then creates an additional three copies of your data using LRS in a separate Azure region that’s hundreds of miles away from the primary region.
			  
			  GZRS creates three copies of your data in three availability zones in the primary region using ZRS. It then creates three copies of your data using LRS in a secondary region that is hundreds of miles away from the primary region. #flashcard
		- -
	- Skill 2.4: Describe Azure identity, access, and security
		- -
			- About RBAC in Azure #flashcard
			  id:: f8c4258c-14d1-4cfd-85bc-56fdf8c10ff8
				- RBAC includes many built-in roles. Three of these built-in roles apply to all Azure resources:
				  
				  Owner Members of this role have full access to the resources.
				  
				  Contributor Members of this role can create resources and manage resources, but they cannot delegate that right to anyone else.
				  
				  Reader Members of this role can see Azure resources, but they cannot create, delete, or manage those resources.
				  
				  All the other built-in roles are specific to certain types of Azure resources.
		- -
		- -
			- Mention the RBAC elements #flashcard
			  id:: 80a5694d-88fd-4ea7-81b7-194e35e75b0d
				- There are four elements to RBAC:
				  
				  Security principal The security principal represents an identity. It can be a user, a group, an application (which is called a service principal), or a special AAD entity called a managed identity. A managed identity is how you authorize another Azure service to access your Azure resource.
				  
				  Role A role (sometimes called a role definition) is what defines how the security principal can interact with an Azure resource. For example, a role might define that a security principal can read the properties of a resource but cannot create new resources or delete existing resources.
				  
				  Scope The scope defines the level at which the role is applied, and it specifies how much control the security principal has. For example, if the scope is a resource group, the role defines activities that can be performed on all resources in the resource group.
				  
				  Role assignments Roles are assigned to a security principal at a particular scope, and that’s what ultimately defines the level of access for the security principal.
		- -
		- -
			- Defender for Cloud can help you protect your cloud resources, not only in Azure, but also in Amazon Web Services (AWS) and the Google Cloud Platform (GCP). It can also aid in ensuring regulatory compliance.
			  id:: bd9b57ad-c5dc-4cb7-90eb-e96a011599a1
			  
			  Defender for Cloud provides insight into four different areas:
			  
			  Security posture Provides a Secure Score, which shows the security of your resources. This area also shows a breakdown of management groups, subscriptions, unhealthy resources, and any recommendations.
			  
			  Regulatory Compliance Provides a high-level overview of the regulatory compliance of your Azure resources.
			  
			  Workload protections Shows you the percentage of protection for each of your service types.
			  
			  Firewall Manager Provides insights into the security of your networks in Azure. #flashcard
		- -