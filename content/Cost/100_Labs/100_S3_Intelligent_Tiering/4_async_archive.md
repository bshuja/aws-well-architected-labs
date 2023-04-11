---
title: "Activate the Amazon S3 Intelligent-Tiering optional asynchronous archive tiers"
date: 2023-04-03T26:16:08-04:00
chapter: false
weight: 5
pre: "<b>4. </b>"
---

To save even more on data that doesn’t require immediate retrieval, you can activate the optional asynchronous Archive Access and Deep Archive Access tiers. When these tiers are activated, objects not accessed for 90 consecutive days are automatically moved directly to the Archive Access tier with up to 71% in storage cost savings. Objects are then moved to the Deep Archive Access tier after 180 consecutive days of no access with up to 95% in storage cost savings.

To access objects archived in the optional asynchronous Archive Access and Deep Archive Access tiers, you first need to restore them. Step 6 of this tutorial will guide you through the restore process.

For this workload, we will activate only the Deep Archive Access tier as depicted below:
![Images/S3IntelligentTiering19.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-19.png)

1. If you have logged out of your AWS Management Console session, log back in. Navigate to the [S3 console](https://s3.console.aws.amazon.com/s3/home) and select the Buckets menu option. From the list of available buckets, select the bucket name of the bucket you created in Step 1.
![Images/S3IntelligentTiering20.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-20.png)

2. Select the Properties tab.
![Images/S3IntelligentTiering21.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-21.png)

3. Navigate to the Intelligent-Tiering Archive configurations section and choose Create configuration.
![Images/S3IntelligentTiering22.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-22.png)

4. In the Archive configuration settings section, specify a descriptive Configuration name for your S3 Intelligent-Tiering Archive configuration.
![Images/S3IntelligentTiering23.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-23.png)

5. For this workload, we want to archive only a subset of the dataset based on the object tags. To do so, under Choose a configuration scope, select Limit the scope of this configuration using one or more filters.
In the Object Tags section, choose Add tag, and enter “opt-in-archive” as Key and “true” as Value of the tag.
Make sure that the Status of the configuration is Enable.
![Images/S3IntelligentTiering24.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-24.png)

6. Objects in the S3 Intelligent-Tiering storage class can be archived to the Deep Archive Access tier after they haven’t been accessed for a time between six months and two years. For this workload, we want to archive objects that haven’t been accessed for 6 months, to ensure that we only archive data that is not being used. To do so, in the Archive rule actions section, select Deep Archive Access tier, enter 180 as number of consecutive days without access before archiving the objects to the Deep Archive Access tier, and choose Create.
![Images/S3IntelligentTiering25.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-25.png)

Like this, for every object you create you can define tag key ““opt-in-archive” to identify objects with archive tiering enabled.

Click on **Next Step** to continue to the next section.
{{< prev_next_button link_prev_url="../3_s3_lifecycle/" link_next_url="../5_deep_archive/" />}}