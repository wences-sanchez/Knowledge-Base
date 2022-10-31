title:: Reading 3.1: Storage Types on AWS | Coursera (highlights)
deck:: [[Across-the-Net]]
author:: [[coursera.org]]
full-title:: "Reading 3.1: Storage Types on AWS | Coursera"
category:: #articles
url:: https://www.coursera.org/learn/aws-cloud-technical-essentials/lecture/7WOVN/introduction-to-week-3

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- AWS storage services are grouped into three different categories: block storage, file storage, and object storage. #flashcard
	- -
	- -
		- Understand the Types of High Availability
		  The last challenge to address when having more than one server is the type of availability you need—either be an active-passive or an active-active system. 
		  Active-Passive: With an active-passive system, only one of the two instances is available at a time. One advantage of this method is that for stateful applications where data about the client’s session is stored on the server, there won’t be any issues as the customers are always sent to the same server where their session is stored.Active-Active: A disadvantage of active-passive and where an active-active system shines is scalability. By having both servers available, the second server can take some load for the application, thus allowing the entire system to take more load. However, if the application is stateful, there would be an issue if the customer’s session isn’t available on both servers. Stateless applications work better for active-active systems. #flashcard
	- -
	- -
		- With a traditional approach to scaling, you buy and provision enough servers to handle traffic at its peak. However, this means that at night time, there is more capacity than traffic. This also means you’re wasting money. Turning off those servers at night or at times where the traffic is lower only saves on electricity. 
		  id:: b00dde6a-39d7-431e-bb1c-fd65800679f9
		  
		  The cloud works differently, with a pay-as-you-go model. It’s important to turn off the unused services, especially EC2 instances that you pay for On-Demand. One could manually add and remove servers at a predicted time. But with unusual spikes in traffic, this solution leads to a waste of resources with over-provisioning or with a loss of customers due to under-provisioning. #flashcard
	- -