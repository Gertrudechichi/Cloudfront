Cloudfront is Amazon's Content Network. Edge locations are are physiscal sites which are distributed across the globe.Cloudfront cache contents to users using edge locations and this ensures that contents are delivered to users through caching and this brings about low latency.

This labwork involves uploading an index.html file to an s3 Bucket. The S3 will be setup to work with cloudfront to deliver contents to users.

BELOW IS A STEP BY STEP PROCEDURE THAT WAS ACHIEVED USING THE AWS MANAGEMENT CONSOLE

Navigated to S3 console and created an s3 bucket
![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/01_S3_Bucket%20creation%20cofiguration.png)

All public access was blocked beacuse i wanted the users to access the website directly from the the cached content.
![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/02_Blocking%20of%20Public%20access%20to%20S3%20bucket.png)

Next the index.html file was uploaded into the S3 bucket.Since all public access to the bucket was blocked, the bucket endpoint was not accessible in the browser. As mentioned earlier, the main objective is to allow cloudfront to access the bucket and serve contents to users. 
![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/03_Successful%20creation%20of%20S3%20bucket.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/04_HTML%20file%20upload%20in%20S3%20Bucket.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/05_Cloudfront%20distribution%20configuration%20_origin%20domain%20indiacted.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/06_Origin%20access%20creation.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/07_Origin%20access%20successfully%20selected.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/08_Default%20configurations.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/09_Firewall%20configuration.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/10_Successful%20creation%20of%20distribution.png)


![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/11_Updated%20bucket%20policy.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/12_Successful%20editing%20of%20the%20bucket%20policy.png)

![image alt](https://github.com/Gertrudechichi/Cloudfront/blob/c132455b3ea7015982a917af57a615b30d38cfe7/13_Distributed%20omain%20name%20pasted%20on%20the%20browser.png)
