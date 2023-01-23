# Exam Ref AZ-900 Microsoft Azure Fundamentals

deck:: [[O'Reilly-Learning::Exam Ref AZ-900 Microsoft Azure Fundamentals]]\
author:: [[Jim Cheshire]]\
full-title:: "Exam Ref AZ-900 Microsoft Azure Fundamentals"\
category:: #books\
\
tags:: Azure O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9780137955107/)
## Highlights
### Skill 1.2: Describe the benefit of using cloud services
- id:: 63c669fc-ca9e-457a-80c0-e6636137fad0
  
  VMs make it easy to add additional computers when necessary, and they allow you to better manage computer resources such as CPU, disk space, and memory. For that reason, VMs are commonplace in most businesses. #flashcard
-
### Chapter summary
- id:: 63c669fc-a0ca-4eb0-a8dc-05af0e7f3ea2
   What does *tenant* mean (in Azure)? #flashcard 
    The public cloud model is sometimes referred to as a multitenant environment. Multiple companies and users share the same infrastructure. VMs and other infrastructure are allocated to users as they need them, and when they no longer need them, they are returned to the pool to be used by other users. The network is available publicly over the internet, but you do have the ability to put security methods in place to control access to your resources.
     The private cloud model is sometimes referred to as a single-tenant environment. All infrastructure is private to an individual or a company, and the network is only available within the private cloud itself. It is not exposed to the internet. In many cases, the infrastructure used in a private cloud is owned by the company, but not always. It’s possible to host a private cloud in a third-party data center.
-
### Skill 2.1: Describe the core architectural components of Azure
- id:: 63c669fc-6518-403e-95a7-78df031f0738
  
  Availability zones aren’t available in all Azure regions, nor are they available for all Azure services in regions that support them. For the most up-to-date list of availability zone-enabled regions and services, see https://bit.ly/az900-azones. #flashcard
-
- id:: 63c669fc-4119-418c-bb33-38a2fea9460e
  
  Customers only see Regions
     When a customer is creating Azure resources, only the region is visible. The concept of geographies is an internal implementation of Azure that customers don’t really have visibility of when using Azure. Customers also don’t have visibility into the concept of regional pairs, but they can see each region within a regional pair. #flashcard
-
### Skill 2.2: Describe Azure compute and networking services
- id:: 63c669fc-7189-4964-86c1-71894bffd0e1
   When to use AKS in Azure #flashcard 
    ACI is designed to work with simple applications. You can define a container group and run multiple containers within an ACI instance, but ACI isn’t a good choice for you if you have an application that is used heavily by many people and that might need to take advantage of scaling. Instead, Azure Kubernetes Service (AKS) would be a better choice.
-
- id:: 63c669fc-0cc5-4181-a895-7523d98e8625
  
  The new VM is a guest on a physical computer in an Azure datacenter. In that datacenter is a physical rack of computer servers, and our VM is hosted on one of those servers. The host computer is managed by Microsoft, but you manage the VM because this is an IaaS offering in Azure. #flashcard
-
- id:: 63c669fc-8970-42b2-8506-5162f82cb8a5
   Explain what *planned maintenance* is in Azure #flashcard 
    Planned maintenance refers to planned updates that Microsoft makes to the host computer. This includes things like operating system updates, driver updates, and so on. In many cases, updates won’t affect your VM, but if Microsoft installs an update that requires a reboot of the host computer, your VM will be down during that reboot.
-
- id:: 63c669fc-b51f-4d73-bb66-92e174cf71f0
   Explain what *unplanned maintenance* is in Azure #flashcard 
    Azure has underlying systems that constantly monitor the health of computer components. If one of these underlying systems detects that a component within the host computer might fail soon, Azure will flag the computer for unplanned maintenance. In an unplanned maintenance event, Azure will attempt to move your VM to a healthy host computer. When it does this, it preserves the state of the VM, including what’s in memory and any files that are open. It only takes Azure a short time to move the VM, during which time it’s in a paused state. In a case where the move operation fails, the VM will experience unexpected downtime.
-
- id:: 63c669fc-6330-4851-9a1d-4ea80aecdaf3
  
  Azure offers another feature for VMs called scale sets that solves these problems nicely. When you create a scale set, you tell Azure what operating system you want to run and then you tell Azure how many VMs you want in your scale set. You have many other options such as creating a load balancer or gateway and so forth. Azure will create as many VMs as you specify (up to 1,000) in one easy step. #flashcard
-
- id:: 63c669fc-5e5b-45cb-a232-d60ae1cbadd4
  
  This diagram is simplified, but it illustrates the basics of how App Service works. Azure Load Balancer distributes traffic to a special VM within App Service called a front end. The front end is running special software that allows it to effectively distribute traffic to the VMs that are actually running your web app. These VMs run inside of an App Service plan, a logical container for one or more VMs that are running your web app.
     FIGURE 2-20 A high-level representation of Azure App Service #flashcard
-
- id:: 63c669fc-5407-4bf5-bc92-1eb9c5f6750d
  
  Every web app you create in App Service runs inside of an App Service plan. An App Service plan is created within a specific Azure region, and it specifies how many VMs your app runs on and the properties of those VMs. #flashcard
-
- id:: 63c669fc-1d07-4059-b035-e0b2e2d4021e
  
  You are charged for App Service plans even when no web apps are running in them. If you do have web apps in your App Service plan, you are still charged if you stop the web apps. The only way to avoid being billed for an App Service plan is to delete it. #flashcard
-
- id:: 63c669fc-58ef-4430-8525-5682d5cb6e1b
   About the importance of Kubernetes in job offers #flashcard 
    While AKS makes adopting and managing Kubernetes easier, it doesn’t completely obfuscate Kubernetes. To deploy your applications, you still need to understand how to use Kubernetes, and in some cases, you’ll need to use the Kubernetes command line. Azure, however, makes it far easier than doing all the legwork and maintenance yourself
-
- id:: 63c669fc-0a7d-46e7-96ef-4986cc652ef1
   Explain what is a *site-to-site connection*. #flashcard 
    A site-to-site connection allows you to connect your VNet to an on-premises network using an encrypted VPN connection. Site-to-site connections require you to configure a VPN device on your on-premises network, and that VPN device must have a public-facing IP address. Network traffic between your VNet and your on-premises network travels over an encrypted VPN connection.
-
- id:: 63c669fc-42aa-45e9-80d6-1406a24b28e9
   Explain what is a *point-to-site connection*. #flashcard 
    A point-to-site connection connects your VNet to a single device. That device can be a computer, but it can also be a mobile device, such as a tablet or a smartphone. When using a point-to-site connection, software on the device establishes a VPN connection to VPN Gateway, and all traffic is encrypted and travels over that connection.
-
### Skill 2.3: Describe Azure Storage services
- id:: 63c669fc-ddfb-49ad-8f8e-6534f0dd5ec4
  
  There are two redundancy options designed to replicate your data only in the primary region. They are locally redundant storage (LRS) and zone-redundant storage (ZRS). When using LRS, Azure makes three copies of your data within a single datacenter. ZRS also makes three copies of your data, but each copy is in a separate availability zone in a separate datacenter. #flashcard
-
- id:: 63c669fc-20f2-4c8b-9f00-81910c805727
  
  When you use ZRS, each copy of your data is in a separate datacenter because Azure uses availability zones for redundancy. ZRS has the added benefit of protecting your data from a problem impacting a single datacenter, but it won’t protect you from a large-scale disaster in an Azure region. #flashcard
-
- id:: 63c669fc-a592-4c6e-a19d-e2077f4d98d5
  
  Azure can also distribute copies of your data across Azure regions. These options protect you from a large-scale impact in a particular Azure region. Just as with primary-region redundancy, there are two redundancy options for multiple-region redundancy. They are geo-redundant storage (GRS) and geo-zone-redundant storage (GZRS).
     GRS creates three copies of your data in the primary region using LRS. It then creates an additional three copies of your data using LRS in a separate Azure region that’s hundreds of miles away from the primary region.
     GZRS creates three copies of your data in three availability zones in the primary region using ZRS. It then creates three copies of your data using LRS in a secondary region that is hundreds of miles away from the primary region. #flashcard
-
### Skill 2.4: Describe Azure identity, access, and security
- id:: 63c669fc-a967-44d2-a8f6-a2c3e435cbf2
   About RBAC in Azure #flashcard 
    RBAC includes many built-in roles. Three of these built-in roles apply to all Azure resources:
     Owner Members of this role have full access to the resources.
     Contributor Members of this role can create resources and manage resources, but they cannot delegate that right to anyone else.
     Reader Members of this role can see Azure resources, but they cannot create, delete, or manage those resources.
     All the other built-in roles are specific to certain types of Azure resources.
-
- id:: 63c669fc-1587-4b54-b530-4dc8099e064b
   Mention the RBAC elements #flashcard 
    There are four elements to RBAC:
     Security principal The security principal represents an identity. It can be a user, a group, an application (which is called a service principal), or a special AAD entity called a managed identity. A managed identity is how you authorize another Azure service to access your Azure resource.
     Role A role (sometimes called a role definition) is what defines how the security principal can interact with an Azure resource. For example, a role might define that a security principal can read the properties of a resource but cannot create new resources or delete existing resources.
     Scope The scope defines the level at which the role is applied, and it specifies how much control the security principal has. For example, if the scope is a resource group, the role defines activities that can be performed on all resources in the resource group.
     Role assignments Roles are assigned to a security principal at a particular scope, and that’s what ultimately defines the level of access for the security principal.
-
- id:: 63c669fc-9965-4897-84ff-09684d857827
  
  Defender for Cloud can help you protect your cloud resources, not only in Azure, but also in Amazon Web Services (AWS) and the Google Cloud Platform (GCP). It can also aid in ensuring regulatory compliance.
     Defender for Cloud provides insight into four different areas:
     Security posture Provides a Secure Score, which shows the security of your resources. This area also shows a breakdown of management groups, subscriptions, unhealthy resources, and any recommendations.
     Regulatory Compliance Provides a high-level overview of the regulatory compliance of your Azure resources.
     Workload protections Shows you the percentage of protection for each of your service types.
     Firewall Manager Provides insights into the security of your networks in Azure. #flashcard
-