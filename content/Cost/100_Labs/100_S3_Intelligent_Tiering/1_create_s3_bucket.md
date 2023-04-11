---
title: "Create an Amazon S3 bucket"
date: 2023-04-03T26:16:08-04:00
chapter: false
weight: 2
pre: "<b>1. </b>"
---

1. Log into the [AWS Management Console](https://console.aws.amazon.com/) using your account information. From the AWS console services search bar, enter ‘S3’. Under the services search results section, select S3 to go to Amazon S3 console.
![Images/S3IntelligentTiering02.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-02.png)

2. Create an S3 bucket - In the Amazon S3 menu on the left, choose Buckets, and then choose Create bucket in the Buckets section.
![Images/S3IntelligentTiering03.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-03.png)

3. Enter a descriptive name for your bucket. Bucket names are globally unique; if you encounter an error with the name you selected, please try another combination. Select which AWS Region you would like your bucket created in.
![Images/S3IntelligentTiering04.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-04.png)

4. Next, leave the default setting with ACLs disabled as [ACLs](https://docs.aws.amazon.com/AmazonS3/latest/userguide/acl-overview.html) are not necessary for this lab; access to the bucket and its objects is specified using only [bucket policies](https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html).
![Images/S3IntelligentTiering05.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-05.png)

5. The default Block Public Access setting is appropriate for this lab, so leave the default settings in this section.
![Images/S3IntelligentTiering06.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-06.png)

6. Then, add a [bucket tag](https://docs.aws.amazon.com/AmazonS3/latest/userguide/CostAllocTagging.html) to help track costs associated with this workload. AWS uses the bucket tags to organize your resource costs on your [cost allocation report](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/configurecostallocreport.html), to make it easier for you to categorize and track your AWS costs. For more information, see [Using Cost Allocation](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) Tags in the AWS Billing User Guide.
![Images/S3IntelligentTiering07.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-07.png)

7. Now enable Default encryption for the bucket. The settings here will apply to any objects uploaded to the bucket where you have not defined at-rest encryption details during the upload process. For this lab, enable Server-side encryption leveraging Amazon S3 service managed keys (SSE-S3). You can also leverage AWS Key Management Service (AWS KMS). For more information about how Amazon S3 uses AWS KMS, see the [AWS Key Management Service Developer Guide](https://docs.aws.amazon.com/kms/latest/developerguide/services-s3.html).![Images/S3IntelligentTiering08.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-08.png)

8. In the Advanced settings, for this workload we don’t need Object Lock, so leave it disabled and create the S3 bucket by choosing Create bucket.
![Images/S3IntelligentTiering09.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-09.png)

Click on **Next Step** to continue to the next section.
{{< prev_next_button link_prev_url="../0_intelli_tiering_overview/" link_next_url="../2_upload_data/" />}}