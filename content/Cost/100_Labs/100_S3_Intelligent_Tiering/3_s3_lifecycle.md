---
title: "Transition objects to the Amazon S3 Intelligent-Tiering storage class using Amazon S3 lifecycle"
date: 2023-04-03T26:16:08-04:00
chapter: false
weight: 4
pre: "<b>3. </b>"
---

When data is programmatically uploaded to Amazon S3, some clients might not be compatible with the S3 Intelligent-Tiering storage class. As a result, those clients will upload the data in the [Amazon S3 Standard storage class](https://aws.amazon.com/s3/storage-classes/). In this case, you can use [Amazon S3 Lifecycle](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html) to immediately transition objects from the S3 Standard storage class to the S3 Intelligent-Tiering storage class.

In this section, you will learn how to set an S3 Lifecycle configuration on your bucket.

1. If you have logged out of your AWS Management Console session, log back in. Navigate to the [S3 console](https://s3.console.aws.amazon.com/s3/home) and select the Buckets menu option. From the list of available buckets, select the bucket name of the bucket you created in Step 1.
![Images/S3IntelligentTiering15.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-15.png)

2. Select the Management tab and then select Create lifecycle rule in the Lifecycle rules section.
![Images/S3IntelligentTiering16.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-16.png)

3. **Create lifecycle rule**
When you create an S3 Lifecycle rule, you have the option to limit the scope of the rule by prefix, tag, or object size specifying a minimum and a maximum object size between 0 bytes and up to 5 TB. By default, objects smaller than 128 KB are never transitioned to the S3 Intelligent-Tiering storage class because they are not eligible for auto tiering.

For this workload we want to apply the Lifecycle rule to all objects in the bucket and therefore we won’t apply any filters.

* Enter a descriptive Lifecycle rule name.
* Select Apply to all objects in the bucket.
* Select the I acknowledge that this rule will apply to all objects in the bucket checkbox.
* In the Lifecycle rule actions, select the Move current versions of objects between storage classes checkbox. For more information, see [Using versioning in S3 buckets](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html).
* In the Transition current versions of objects between storage classes section, select Intelligent-Tiering as Choose storage class transitions, and input 0 as Days after object creation.
* Finally, choose Create rule.
![Images/S3IntelligentTiering17.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-17.png)

In this step, we created a Lifecycle rule to immediately transition files uploaded in the S3 Standard storage class into the S3 Intelligent-Tiering storage class.
![Images/S3IntelligentTiering18.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-18.png)

Click on **Next Step** to continue to the next section.
{{< prev_next_button link_prev_url="../2_upload_data/" link_next_url="../4_async_archive/" />}}

