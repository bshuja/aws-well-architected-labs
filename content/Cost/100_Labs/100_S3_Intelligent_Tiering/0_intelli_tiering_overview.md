---
title: "Amazon S3 Intelligent-Tiering Overview"
date: 2023-04-03T26:16:08-04:00
chapter: false
weight: 1
pre: "<b>1. </b>"
---

The S3 Intelligent-Tiering storage class monitors access patterns and automatically moves objects between three access tiers without performance impact or operational overhead for a low monthly object monitoring and automation charge. S3 Intelligent-Tiering is the ideal storage class for data with unknown, changing, or unpredictable access patterns, independent of object size or retention period

S3 Intelligent-Tiering automatically stores objects in three access tiers:
* Frequent Access tier optimized for frequently accessed data
* Lower-cost Infrequent Access tier optimized for infrequently accessed data
* Very-low-cost Archive Instant Access tier optimized for rarely accessed data

For a small monthly object monitoring and automation charge, S3 Intelligent-Tiering moves objects that have not been accessed for 30 consecutive days to the Infrequent Access tier for savings of 40%; and after 90 days of no access, objects are moved to the Archive Instant Access tier with savings of 68%. If the objects are accessed later, S3 Intelligent-Tiering automatically moves the objects back to the Frequent Access tier.

To save more on storage cost that doesn’t require immediate retrieval, you can activate the optional asynchronous Archive Access and Deep Archive Access tiers. When turned on, objects not accessed for 90 days are moved directly to the Archive Access Tier (bypassing the automatic Archive Instant Access tier) and the Deep Archive Access tier after 180 days. To retrieve an object stored in the optional Archive Access tier or Deep Archive Access tier, you must initiate the [restore request](https://docs.aws.amazon.com/AmazonS3/latest/userguide/restoring-objects.html) and wait until the object is moved into the Frequent Access tier.

![Images/S3IntelligentTiering01.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-01.png)

You can use S3 Intelligent-Tiering as the default storage class for virtually any workload, especially data lakes, data analytics, new applications, and user-generated content.

{{< prev_next_button link_prev_url="../" link_next_url="../1_create_s3_bucket/" />}}