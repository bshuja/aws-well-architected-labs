---
title: "Level 100: Amazon S3 Intelligent Tiering"
menutitle: "Level 100: Amazon S3 Intelligent Tiering"
date: 2023-04-03T26:16:08-04:00
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

## Well-Architected Best Practices
This lab helps you to exercise the following Well-Architected Best Practices:
* [COST06-BP03](https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/cost_type_size_number_resources_metrics.html) - **Select resource type, size, and number automatically based on metrics**

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
