Project Description: Making Your S3 Static Website Accessible to Everyone with CloudFront while maintaining its privacy.

Introduction:
When hosting a static website on Amazon S3, you may want to make it accessible to everyone while still keeping the content private and secure. One way to achieve this is by leveraging Amazon CloudFront, a content delivery network (CDN) that provides low-latency and high-speed content delivery.

Step 1: Set Up Your S3 Bucket
Create an S3 bucket and enable website hosting for it under properties.
Upload your static website files to the S3 bucket.
Configure the bucket policy to deny public access to the content.

Step 2: Create a CloudFront Distribution
Go to the CloudFront console and click "Create Distribution"
Click on Origin domain name and select your s3 bucket as the origin domain
Select the origin access as OAC, it'll prompt you to create control setting
click on control settings keep everything as default and press create button
After OAC has been created, you'll be prompted to update your s3 bucket policy for cloudfront to access contents in s3 bucket
Update the poicy under permissions tab for s3 bucket, navigate back to cloudfront distribution
Keep all the other setting as default and select Default root object as index.html, then click create distribution
Once your Distribution is enabled, copy the Distribution domain name in browserand you'll be able to access your website 

What is OAC:  Origin Access Control (OAC) in CloudFront provides an additional layer of security by allowing you to control access to your origin server and restrict it to specific IP addresses or referrers. It helps protect your content and ensure that only authorized users can access it through CloudFront.

Conclusion:
By following these steps, you have successfully configured Amazon CloudFront to serve your S3 static website while keeping its content private. CloudFront acts as a secure and scalable CDN, ensuring fast and reliable content delivery to users around the world. With this setup, you can confidently host and share your static website without compromising its security.

Important: This website can additionally be enhanced to restrict access from particular countries based on your use case leveraging Geo-Restriction feature of cloudfront.

Happy hosting with Amazon S3 and CloudFront!





