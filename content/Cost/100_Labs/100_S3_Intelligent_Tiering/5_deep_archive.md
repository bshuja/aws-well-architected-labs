---
title: "Upload a file with the opt-in Deep Archive Access tier enabled"
date: 2023-04-05T11:16:09-04:00
chapter: false
weight: 6
pre: "<b>5. </b>"
---

In section 4, we enabled the Deep Archive Access tier only for objects with tag “opt-in-archive:true”. Now you’re going to learn how to apply the correct tag during the upload process to enable the Deep Archive Access tier.

1. From the AWS Management Console session, navigate to the [S3 console](https://s3.console.aws.amazon.com/s3/home) and select the Buckets menu option. From the list of available buckets, select the bucket name of the bucket you created in Step 1.

2. Next, select the Objects tab. Then, from within the Objects section, choose Upload.
![Images/S3IntelligentTiering26.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-26.png)

3. Then, choose Add files. Navigate to your local file system to locate the file you would like to upload. Select the appropriate file and then choose Open. Your file will be listed in the Files and folders section.
![Images/S3IntelligentTiering27.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-27.png)

4. In the Properties section, select Intelligent-Tiering. For more information about the Amazon S3 Intelligent-Tiering storage class, see the [Amazon S3 User Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/intelligent-tiering.html).
![Images/S3IntelligentTiering28.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-28.png)

5. Because we want the file to be archived after 6 months of no access, in the Tags – optional section we select Add tag with Key “opt-in-archive” and Value “true”, and choose Upload.
![Images/S3IntelligentTiering29.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-29.png)