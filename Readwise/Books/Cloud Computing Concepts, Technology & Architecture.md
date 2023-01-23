# Cloud Computing: Concepts, Technology & Architecture

deck:: [[Other-Books::Cloud Computing: Concepts, Technology & Architecture]]\
author:: [[Thomas Erl]]\
full-title:: "Cloud Computing: Concepts, Technology & Architecture"\
category:: #books\
\
tags:: cloud o'reilly-learning  

![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323849/cover-image-9780133387513_4jAE372.jpg)
## Highlights
#### Chapter 3. Understanding Cloud Computing
- id:: 63c669e7-d7d1-4268-9953-2499664a9c2d
   Define cloud computing #flashcard 
    *“Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction. This cloud model is composed of five essential characteristics, three service models, and four deployment models.”*
     This book provides a more concise definition:
     *“Cloud computing is a specialized form of distributed computing that introduces utilization models for remotely provisioning scalable and measured resources.”*
  
    ([View Highlight](https://read.readwise.io/read/01gp0qpp0v11jvvp11mwddtgc6))
-
- id:: 63c669e7-b031-4555-a69b-d56f1ee16285
  
  Grid Computing
     A computing grid (or “computational grid”) provides a platform in which computing resources are organized into one or more logical pools. These pools are collectively coordinated to provide a high performance distributed grid, sometimes referred to as a “super virtual computer.” Grid computing differs from clustering in that grid systems are much more loosely coupled and distributed. As a result, grid computing systems can involve computing resources that are heterogeneous and geographically dispersed, which is generally not possible with cluster computing-based systems. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp0rjcx8z1p9e615009ph07k))
-
- id:: 63c669e7-8e91-4ff4-a102-d4c1d75f8072
   Which type of scaling is more expensive, in Cloud Computing? #flashcard 
    [Table 3.1](https://readwise.io/reader/document_raw_content/24323849#ch03tab01) provides a brief overview of common pros and cons associated with horizontal and vertical scaling.
     ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323849/a03tab01-03tab01.jpg)
     **Table 3.1** A comparison of horizontal and vertical scaling
  
    ([View Highlight](https://read.readwise.io/read/01gp0snce9z1bf78jvfd5szw8m))
-
- id:: 63c669e7-2ffa-448f-a318-183ddd2af01c
  
  The driving motivation behind cloud computing is to provide IT resources as services that encapsulate other IT resources, while offering functions for clients to use and leverage remotely. A multitude of models for generic types of cloud services have emerged, most of which are labeled with the “as-a-service” suffix. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp0t73nbttgdsb7fme71dbpf))
-
- id:: 63c669e7-50dc-46aa-b07f-5636912bce4c
   Benefits of the cloud (academically described): #flashcard 
    Common measurable benefits to cloud consumers include:
     • On-demand access to pay-as-you-go computing resources on a short-term basis (such as processors by the hour), and the ability to release these computing resources when they are no longer needed.
     • The perception of having unlimited computing resources that are available on demand, thereby reducing the need to prepare for provisioning.
     • The ability to add or remove IT resources at a fine-grained level, such as modifying available storage disk space by single gigabyte increments.
     • Abstraction of the infrastructure so applications are not locked into devices or locations and can be easily moved if needed.
  
    ([View Highlight](https://read.readwise.io/read/01gp0tggj0yw2xyejzhx8r4mah))
-
- id:: 63c669e7-2945-469e-a955-cbf3df42a320
  
  A simple example of usage demand fluctuations throughout a 24 hour period is provided in [Figure 3.8](https://readwise.io/reader/document_raw_content/24323849#ch03fig08).
     ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323849/a03fig08-03fig08.jpg)
     **Figure 3.8** An example of an organization’s changing demand for an IT resource over the course of a day.
     The inherent, built-in feature of clouds to provide flexible levels of scalability to IT resources is directly related to the aforementioned proportional costs benefit. Besides the evident financial gain to the automated reduction of scaling, the ability of IT resources to always meet and fulfill unpredictable usage demands avoids potential loss of business that can occur when usage thresholds are met. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp0v074arxt0239q6scaxbe3))
-
- id:: 63c669e7-48c5-4547-b2ac-37536ff34837
  
  Summary of Key Points
     • Cloud environments are comprised of highly extensive infrastructure that offers pools of IT resources that can be leased using a pay-for-use model whereby only the actual usage of the IT resources is billable. When compared to equivalent on-premise environments, clouds provide the potential for reduced initial investments and operational costs proportional to measured usage.
     • The inherent ability of a cloud to scale IT resources enables organizations to accommodate unpredictable usage fluctuations without being limited by pre-defined thresholds that may turn away usage requests from customers. Conversely, the ability of a cloud to decrease required scaling is a feature that relates directly to the proportional costs benefit.
     • By leveraging cloud environments to make IT resources highly available and reliable, organizations are able to increase quality-of-service guarantees to customers and further reduce or avoid potential loss of business resulting from unanticipated runtime failures. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp0vb60fys458tgr6t2npgv0))
-
- id:: 63c669e7-dbec-4acd-abde-e48719c07c49
   The importance of a Content Delivery Network in Cloud Computing #flashcard 
    • Longer geographic distances between the cloud consumer and cloud provider can require additional network hops that introduce fluctuating latency and potential bandwidth constraints.
     The latter scenario is illustrated in [Figure 3.10](https://readwise.io/reader/document_raw_content/24323849#ch03fig10).
     ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323849/a03fig10-03fig10.jpg)
     **Figure 3.10** An unreliable network connection compromises the quality of communication between cloud consumer and cloud provider environments.
  
    ([View Highlight](https://read.readwise.io/read/01gp0vwg29cnswdx2k00b4bg1q))
-
#### Chapter 4. Fundamental Concepts and Models
##### 4.1. Roles and Boundaries
##### 4.2. Cloud Characteristics
- id:: 63c669e7-d3bd-478f-a63c-0980df34f159
  
  Multitenancy (and Resource Pooling)
     The characteristic of a software program that enables an instance of the program to serve different consumers (tenants) whereby each is isolated from the other, is referred to as *multitenancy*. A cloud provider pools its IT resources to serve multiple cloud service consumers by using multitenancy models that frequently rely on the use of virtualization technologies. Through the use of multitenancy technology, IT resources can be dynamically assigned and reassigned, according to cloud service consumer demands.
     Resource pooling allows cloud providers to pool large-scale IT resources to serve multiple cloud consumers. Different physical and virtual IT resources are dynamically assigned and reassigned according to cloud consumer demand, typically followed by execution through statistical multiplexing. Resource pooling is commonly achieved through multitenancy technology, and therefore encompassed by this multitenancy characteristic. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp6rwk8nyppegmv6hsc828wj))
-
- id:: 63c669e7-6f5c-47f9-bc02-20e45a992297
  
  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323849/a04fig09-04fig09.jpg)
     **Figure 4.9** In a multitenant environment, a single instance of an IT resource, such as a cloud storage device, serves multiple consumers.
     As illustrated in [Figure 4.9](https://readwise.io/reader/document_raw_content/24323849#ch04fig09), multitenancy allows several cloud consumers to use the same IT resource or its instance while each remains unaware that it may be used by others. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp6rvkx0ras7hnvhes2rwak2))
-
##### 4.3. Cloud Delivery Models
- id:: 63c669e7-ca23-44e5-bd3f-3082d1071adc
   Define PaaS #flashcard 
    The PaaS delivery model represents a pre-defined “ready-to-use” environment typically comprised of already deployed and configured IT resources. Specifically, PaaS relies on (and is primarily defined by) the usage of a ready-made environment that establishes a set of pre-packaged products and tools used to support the entire delivery lifecycle of custom applications.
  
    ([View Highlight](https://read.readwise.io/read/01gp6s9x9q8yfnawpe51dffjmt))
-
- id:: 63c669e7-2905-4c85-abbe-8c6a20783c2e
  
  Summary of Key Points
     • The IaaS cloud delivery model offers cloud consumers a high level of administrative control over “raw” infrastructure-based IT resources.
     • The PaaS cloud delivery model enables a cloud provider to offer a pre-configured environment that cloud consumers can use to build and deploy cloud services and solutions, albeit with decreased administrative control.
     • SaaS is a cloud delivery model for shared cloud services that can be positioned as commercialized products hosted by clouds.
     • Different combinations of IaaS, PaaS, and SaaS are possible, depending on how cloud consumers and cloud providers choose to leverage the natural hierarchy established by these base cloud delivery models. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp6ssw7x1s9sgpxdwg1k2wwv))
-
##### 4.4. Cloud Deployment Models
- id:: 63c669e7-8022-43c7-999c-037705ccdd32
  
  A hybrid cloud is a cloud environment comprised of two or more different cloud deployment models. For example, a cloud consumer may choose to deploy cloud services processing sensitive data to a private cloud and other, less sensitive cloud services to a public cloud. The result of this combination is a hybrid deployment model ([Figure 4.20](https://readwise.io/reader/document_raw_content/24323849#ch04fig20)).
     ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323849/a04fig20-04fig20.jpg)
     **Figure 4.20** An organization using a hybrid cloud architecture that utilizes both a private and public cloud. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp6tjy3wkqa1bpd7wknm7n0e))
-
- id:: 63c669e7-4931-432f-94ce-289b5dab90ab
  
  Summary of Key Points
     • A public cloud is owned by a third party and generally offers commercialized cloud services and IT resources to cloud consumer organizations.
     • A private cloud is owned by an individual organization and resides within the organization’s premises.
     • A community cloud is normally limited for access by a group of cloud consumers that may also share responsibility in its ownership.
     • A hybrid cloud is a combination of two or more other cloud deployment models. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp6tnkcfme8b7f9fzxfqs36j))
-
#### Chapter 5. Cloud-Enabling Technology
##### 5.1. Broadband Networks and Internet Architecture
- id:: 63c669e7-46e8-4379-b862-8788b50e0e65
  
  Worldwide connectivity is enabled through a hierarchical topology composed of Tiers 1, 2, and 3 ([Figure 5.2](https://readwise.io/reader/document_raw_content/24323849#ch05fig02)). The core Tier 1 is made of large-scale, international cloud providers that oversee massive interconnected global networks, which are connected to Tier 2’s large regional providers. The interconnected ISPs of Tier 2 connect with Tier 1 providers, as well as the local ISPs of Tier 3. Cloud consumers and cloud providers can connect directly using a Tier 1 provider, since any operational ISP can enable Internet connection.
     ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323849/a05fig02-05fig02.jpg)
     **Figure 5.2** An abstraction of the internetworking structure of the Internet. #flashcard 
  
  
    ([View Highlight](https://read.readwise.io/read/01gp6vq0m40tzyx3xa8x188sxj))
-
- id:: 63c669e7-9822-4430-9bd2-9c420134b140
   A comparison of on-premise and cloud-based internetworking. #flashcard 
    ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323849/a05tab01-05tab01.jpg)
  
    ([View Highlight](https://read.readwise.io/read/01gp929ewppq40hskr5t8d9ya1))
-