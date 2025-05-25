AWS CLOUDFRONT


![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/65ba834f6fe779baad1260a8a2ad2647de1d3da1/amazon%20cloudfront.png)



Networking is a very essential concept in AWS. The AWS global infrastructure is very intriguing and what catches my attention the most about the global infrastructure is the Amazon CloudFront which is a content delivery network. 

A cooperate organization can have its Local Area Network for effective collaboration among teams. The internet, which is a Wide Area Network has a lot of IP addresses representing several applications hosted on servers and made publicly accessible. Just like the internet, which is a Wide Area Network, A Content Delivery Network, CloudFront can also be considered as a Wide Area Network that is not restricted to any region, availability zone or datacenter. AWS CloudFront spans through multiple regions.

Just like a network mainly comprise of a router and nodes or a network may comprise of a VPC and an internet gateway. A Content Delivery Network has a gateway which is the CloudFront and its corresponding nodes which are the edge locations. The CloudFront representing the gateway or a checkpoint can access an origin server like S3 if and only if the origin server is configured to permit access to the CloudFront.  The origin access control policy is attached to the s3 bucket and this is a security mechanism for CloudFront to access the origin server content.

Anytime a user tries to access a particular content from the browser, the request is directed to the Content Delivery Network with CloudFront as the checkpoint and its edge locations. if the edge location has cached contents from the origin server, the contents are served to the user with low latency, hence increased performance. However, if there is no cached contents at the edge location, CloudFront , the gateway of the network will have to access the origin server for its contents. Since CloudFront is a managed service by AWS, the routing of the packet of data from the origin server to the edge location is handled by AWS and AWS routes the server contents to the nearest edge location and from there, the contents will be accessible by the user.









This labwork involves uploading an index.html file to an s3 Bucket. The S3 was setup to work with cloudfront to deliver contents to users.
The step by step procedure that was involved is shown below. 






















Navigated to S3 console and created an s3 bucket



![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/01_S3_Bucket%20creation%20cofiguration.png)

All public access was blocked beacuse i wanted the users to access the website directly from the the cached content.



![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/02_Blocking%20of%20Public%20access%20to%20S3%20bucket.png)




Next the index.html file was uploaded into the S3 bucket.Since all public access to the bucket was blocked, the bucket endpoint was not accessible in the browser. As mentioned earlier, the main objective is to allow cloudfront to access the bucket and serve contents to users. 



![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/03_Successful%20creation%20of%20S3%20bucket.png)





The file was successfully uploaded into the bucket as shown.




![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/04_HTML%20file%20upload%20in%20S3%20Bucket.png)




The s3 bucket thet was created was selected as the origin domain .




![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/05_Cloudfront%20distribution%20configuration%20_origin%20domain%20indiacted.png)





Other configurations we set as shown below  and teh distribution was successfully created


![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/06_Origin%20access%20creation.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/07_Origin%20access%20successfully%20selected.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/08_Default%20configurations.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/09_Firewall%20configuration.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/10_Successful%20creation%20of%20distribution.png)



The bucket poolicy was updated to allow cloudfront to access the contents of the bucket








![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/11_Updated%20bucket%20policy.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/12_Successful%20editing%20of%20the%20bucket%20policy.png)




The distributed domain name was copied and pasted in the browser and it displayed the static website.








![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/13_Distributed%20omain%20name%20pasted%20on%20the%20browser.png)
