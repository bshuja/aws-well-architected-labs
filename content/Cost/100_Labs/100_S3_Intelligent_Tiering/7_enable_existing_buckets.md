---
title: "Enable S3 Intelligent tiering for already existing buckets"
date: 2023-04-03T26:16:08-04:00
chapter: false
weight: 8
pre: "<b>7. </b>"
---

1. Login to the S3 Console, you will see a list of buckets, I have created a bucket for this exercise with some objects, for this step, the bucket I am going to use is the bucket name is s3-standard-tier-bucket. Click on the bucket name.
![Images/S3IntelligentTiering35.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-35.png)

2. Open the Management Tab and select create a new Lifecycle rule.
![Images/S3IntelligentTiering36.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-36.png)

3. Choose a name for the lifecycle rule, select as scope Apply to all objects in the bucket, acknowledge that this rule will apply to all objects in the bucket, choose as Lifecycle rule action Move current versions of objects between storage classes 
![Images/S3IntelligentTiering37.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-37.png)

4. Scroll down, and choose as storage class transitions Intelligent Tiering from the drop-down menu, and select to 0 and click on Create Rule
![Images/S3IntelligentTiering38.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-38.png)

5. You have now created a lifecycle rule that will trigger every day at midnight UTC, transitioning automatically your objects to the intelligent tiering storage class. 
![Images/S3IntelligentTiering39.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-39.png)


[Considerations](https://catalog.us-east-1.prod.workshops.aws/workshops/42c0fe7e-8d1c-4d5f-8b48-c818c7952242/en-US/s3/intelligent-tiering/intelligent-tiering#considerations)

1. You could consider enabling intelligent tiering on every new bucket that is created in your accounts. Intelligent tiering charges a monitoring fee, see the [pricing page](https://aws.amazon.com/s3/pricing/)  for more details.

2. The Amazon S3 Intelligent-Tiering storage class is designed to optimize storage costs by automatically moving data to the most cost-effective access tier when access patterns change, i.e. objects become colder, in that they are accessed less.

3. You cannot apply a lifecycle policy and move back from intelligent tiering to the standard storage class. You will need to re-upload the objects if needed. See [Transitioning objects using Amazon S3 Lifecycle](https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html)  for more details.

4. You can then measure savings using Cost Explorer or the Cost and Usage Report (CUR). Cost Explorer and CUR billing data are delayed by ~48 hours, after ~2 days you will be able to visualize the savings. This is how Cost Explorer will look when introducing intelligent tiering on s3 buckets in the example below:
![Images/S3IntelligentTiering40.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-40.png)

Click on **Next Step** to continue to the next section.
{{< prev_next_button link_prev_url="../6_restore_data/" link_next_url="../8_clean_up/" />}}