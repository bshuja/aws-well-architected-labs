---
title: "Level 100: Amazon S3 Intelligent Tiering"
#menutitle: "Lab #3"
date: 2023-04-05T11:16:08-04:00
chapter: false
weight: 9
hidden: false
---
## Last Updated
April 2023

## Authors
* **Mugdha Vartak**, AWS Solutions Architect
* **Bilal Shuja**, AWS Technical Account Manager

## Contributor
* **Ben Mergen**, Sr Cost Lead SA WA.

## Feedback
If you wish to provide feedback on this lab, there is an error, or you want to make a suggestion, please email: costoptimization@amazon.com.

## Amazon S3 Intelligent-Tiering Overview
The S3 Intelligent-Tiering storage class monitors access patterns and automatically moves objects between three access tiers without performance impact or operational overhead for a low monthly object monitoring and automation charge. S3 Intelligent-Tiering is the ideal storage class for data with unknown, changing, or unpredictable access patterns, independent of object size or retention period

S3 Intelligent-Tiering automatically stores objects in three access tiers:
* Frequent Access tier optimized for frequently accessed data
* Lower-cost Infrequent Access tier optimized for infrequently accessed data
* Very-low-cost Archive Instant Access tier optimized for rarely accessed data

For a small monthly object monitoring and automation charge, S3 Intelligent-Tiering moves objects that have not been accessed for 30 consecutive days to the Infrequent Access tier for savings of 40%; and after 90 days of no access, objects are moved to the Archive Instant Access tier with savings of 68%. If the objects are accessed later, S3 Intelligent-Tiering automatically moves the objects back to the Frequent Access tier.

To save more on storage cost that doesn’t require immediate retrieval, you can activate the optional asynchronous Archive Access and Deep Archive Access tiers. When turned on, objects not accessed for 90 days are moved directly to the Archive Access Tier (bypassing the automatic Archive Instant Access tier) and the Deep Archive Access tier after 180 days. To retrieve an object stored in the optional Archive Access tier or Deep Archive Access tier, you must initiate the [restore request](https://docs.aws.amazon.com/AmazonS3/latest/userguide/restoring-objects.html) and wait until the object is moved into the Frequent Access tier.

![Images/S3IntelligentTiering01.png](/Cost/100_S3_Intelligent_Tiering/Images/S3-IntelligentTiering-01.png)

You can use S3 Intelligent-Tiering as the default storage class for virtually any workload, especially data lakes, data analytics, new applications, and user-generated content.

## Introduction
This hands-on lab will guide you through the steps to configure **S3 intelligent-tiering** to move objects within Amazon S3 storage tiers automatically through the AWS Console. The skills you learn will help you automate the storage cost optimization based on your access patterns in alignment with your business requirements.

## Goals
* Familiarize with Amazon S3 Intelligent Tiering object storage class 
* Configure a lifecycle policy to transition to [S3 Intelligent tiering](https://aws.amazon.com/s3/storage-classes/intelligent-tiering/) all objects (new and existing).


## Prerequisites
* An [AWS account(https://signin.aws.amazon.com/signin?redirect_uri=https%3A%2F%2Fportal.aws.amazon.com%2Fbilling%2Fsignup%2Fresume&client_id=signup)]
* [AWS IAM](https://aws.amazon.com/iam/) user/role with permission to create/modify an Amazon S3 bucket

## Costs
* S3 Intelligent-Tiering [Pricing](https://aws.amazon.com/s3/pricing/) page

## Time to complete

The lab should take approximately 30 minutes to complete

## Steps
{{% children  /%}}

{{< prev_next_button link_next_url="./1_create_s3_bucket/" button_next_text="Start Lab" first_step="true" />}}
