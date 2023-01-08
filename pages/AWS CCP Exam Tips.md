tags:: AWS 
deck:: [[AWS::CCP::Tips]]

-
- ## Tips from UNIR AWS Course
	- {{cloze AWS Cost Explorer}} allows you to track expenses over time. #flashcard
	  id:: 63566176-c3ac-492c-a8a7-3f1130c37573
-
- ## Tips from ACloudGuru Mock Exams
	- "The {{cloze configuration of infrastructure devices}} refers to the hardware-related issues, not to software management" #flashcard
	  id:: 63567775-8ef7-4d7a-b20c-e138cffe2f20
	- The {{cloze AWS Trust & Safety Team}} is the one whom contact, for example, for hack attacks. #flashcard
	  id:: 635677bf-1c53-4d40-944e-1615411866b8
	- You can find users' credentials, for compliance, in {{cloze IAM Credential Report}} #flashcard
	  id:: 635662d5-8ee4-453c-ac59-4f7bcbb8a8e9
	- What is the role of S3 Transfer Acceleration? #flashcard
	  id:: 635679b8-fb69-433e-a65d-2af68103df31
		- S3 Transfer Acceleration improves content uploads and downloads to and from S3 buckets and is not responsible for serving up website content.
	- AWS doesn't provide {{cloze a help desk service}} for your internals #flashcard
	  id:: 635679d4-4273-43c2-9ed4-9cd3f61a701c
		- The company will still be responsible for maintaining an internal help desk.
	-
	- ¿Pueden ser los despliegues multi-regionales? #flashcard
	  id:: 63aac21a-8828-4675-ab4e-a3785df07251
		- Sí
	- ¿Pueden las subredes comunicarse entre sí? #flashcard
	  id:: 63aac24a-9ea1-467a-acdb-f10b54600176
		- Sí, por defecto las subredes de una misma red o VPC pueden comunicarse entre sí.
	- ¿Puede usarse CloudFront para aumentar la Alta Disponibilidad? #flashcard
	  id:: 63aac285-477d-4ae7-acdf-6f165b7e60e5
		- No, CloudFron solo no puede aumentar la Alta Disponibilidad.
	- ¿Pueden usarse las alarmas de CloudWatch para activar triggers? #flashcard
	  id:: 63aac2d6-42bb-47bf-88f3-14ff6b7ef883
		- Sí, una alarma de CloudWatch se puede usar para activar cualquier trigger
	- ¿A qué pilar del *Well-Architected Framework* le corresponde el descubrimiento de servicios? #flashcard
	  id:: 63aac363-a0cb-4db2-9474-4c25ba3718f8
		- A la eficacia del rendimiento
	-
	- During disaster recovery exercises, you need to re-route traffic from EC2 instances to instances in another Region. With which service can you do this? #flashcard
	  id:: 63bae884-3616-4fc8-a9f1-89e60e453758
		- ~~VPC Peering~~
			- *VPC peering facilitates communication between 2 different VPCs, but it is not a mechanism for disaster recovery. In a disaster situation, the original Region would be out of service.*
		-
		- **Route 53**
			- > Route 53 can be used for disaster recovery by simply shifting traffic to the new Region. Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. It is designed to give developers and businesses an extremely reliable and cost-effective way to route end users to internet applications by translating names (like *[www.example.com](http://www.example.com)*) into the numeric IP addresses (like 192.0.2.1) that computers use to connect to each other. Amazon Route 53 is fully compliant with IPv6 as well.
	- What are the AWS Partner Network (APN) Technology Partners? #flashcard
	  id:: 63b54d0c-6047-4ab6-b8da-cbe16761a81e
		- APN Technology Partners specifically provide new solutions to build on AWS. This may include specific software, hardware, or connectivity services. In this case, since we already have the new system that we want to deploy, an APN Technology Partner wouldn't be useful here, since we only need assistance to deploy the solution. AWS Documentation: [Joining the AWS Partner Network (APN) Strengthens Your Capabilities to Better Serve Customers](https://aws.amazon.com/blogs/apn/joining-the-aws-partner-network-apn-strengthens-your-capabilities-to-better-serve-customers/).
	- What are the AWS Partner Network (APN) Consulting Partners? #flashcard
	  id:: 63b54dc2-04d6-4cbf-b75e-b17722ca31ea
		- APN Consulting Partners include professional services organizations like system integrators, strategic consultancies, agencies, managed service providers (MSPs), and value-added resellers. In this case, we would engage a Consulting Partner to help us deploy a new system to the AWS Cloud. AWS Documentation: [Joining the AWS Partner Network (APN) Strengthens Your Capabilities to Better Serve Customers](https://aws.amazon.com/blogs/apn/joining-the-aws-partner-network-apn-strengthens-your-capabilities-to-better-serve-customers/).
	- Which benefit of cloud computing is demonstrated when you don't have to plan ahead of time how much capacity you will need to run your applications? #flashcard
	  id:: 63b54df3-5ad9-4efb-8b51-22d770f1fcfa
		- ~~Agility~~
			- *The cloud gives you increased agility. All the services you have access to help you innovate faster, giving you speed to market.*
		- **Elasticity**
			- > With elasticity, you do not have to plan ahead of time how much capacity you need. You can provision only what you need, and then grow and shrink based on demand.
	- Are you (as a customer) responsible for network traffic? #flashcard
	  id:: 63b54e70-0369-4734-869b-238d181c6c94
		- Yes. You are responsible for network traffic protection, which includes security group firewall configuration.
	- Upon attempting to create an additional S3 bucket, you realize you have reached your S3 bucket limit in your AWS account. You anticipate creating even more S3 buckets in the future for your photos and documents. Which of the following is the quickest solution? #flashcard
	  id:: 63b54f4e-63f9-43cd-874c-b1a5b7f0be48
		- ~~Simply create the S3 bucket; AWS will automatically override the bucket limit.~~
			- *By default, you can create up to 100 buckets in an AWS account, and that is a limit AWS does not override without officially requesting a service limit increase.*
		- **Submit a service limit increase.**
			- > The key word here is "quickest," and the fastest option is to request a service limit increase at the AWS Support Center.
			  [https://docs.aws.amazon.com/AmazonS3/latest/dev/BucketRestrictions.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/BucketRestrictions.html)
	- What is the maximum number of objects you can store in S3 per AWS account? #flashcard
	  id:: 63b54f8f-cbe2-4136-9471-dbfb66cee043
		- Unlimited
			- >You can store an essentially unlimited number of objects in S3 - either in a single bucket or across multiple in your account.
	- A company would like to reduce operational overhead when operating AWS infrastructure. Which service can help them do this? #flashcard
	  id:: 63b5502a-142c-42ec-a3a3-bc04f672adee
		- **Managed Services**
			- > Managed Services helps you efficiently operate your AWS infrastructure and reduces operational risks and overhead.
-