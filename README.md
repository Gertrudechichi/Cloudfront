

CLOUDFRONT DEMO


Cloudfront is Amazon's Content Network. Edge locations are are physiscal sites which are distributed across the globe.Cloudfront cache contents to users using edge locations and this ensures that contents are delivered to users through caching and this brings about low latency.






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
