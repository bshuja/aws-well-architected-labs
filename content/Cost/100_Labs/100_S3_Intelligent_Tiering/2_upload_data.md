---
title: "Upload data to the Amazon S3 Intelligent-tiering storage class"
date: 2023-04-05T11:16:09-04:00
chapter: false
weight: 3
pre: "<b>2. </b>"
---

Now that your bucket has been created and configured, you are ready to upload data to the Amazon S3 Intelligent-Tiering storage class.

**Upload an object**

1. If you have logged out of your AWS Management Console session, log back in. Navigate to the [S3 console](https://s3.console.aws.amazon.com/s3/home) and select the Buckets menu option. From the list of available buckets, select the bucket name of the bucket you just created.
![Images/S3IntelligentTiering10.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-10.png)

2. Next, select the Objects tab. Then, from within the Objects section, choose Upload.
![Images/S3IntelligentTiering11.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-11.png)

3. Then, in the Upload section, choose Add files. Navigate to your local file system to locate the file you would like to upload. Select the appropriate file, and then choose Open. Your file will be listed in the Files and folders section.
![Images/S3IntelligentTiering12.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-12.png)

4. In the Properties section, select Intelligent-Tiering. Leave the rest of the options on the default settings, and choose Upload.
![Images/S3IntelligentTiering13.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-13.png)

5. After your file upload operations have completed, you will be presented with a summary of the operations indicating if it has completed successfully or if it has failed. In this case, the file has uploaded successfully. Then, choose Close.
![Images/S3IntelligentTiering14.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-14.png)

You have successfully uploaded your file to your bucket using the S3 Intelligent-Tiering storage class. Next, we will discuss transitioning objects that are already stored in the S3 Standard or in the S3 Standard-IA storage classes to the S3 Intelligent-Tiering storage class.