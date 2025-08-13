---
title : "Create job queue"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---



1. Access [AWS BATCH service management console]
  + Click **Job queue**
  + Click **Create**.
![S3](/images/4.s3/CreateJobQueue.png)
  + in the name field, enter **yt-s3-copy-queue**
![S3](/images/4.s3/NameJobQueue.png)
  + in the connected compute environments select **yt-s3-copy**
![S3](/images/4.s3/ConnectComputeEnvironments.png)
  + Click create job queue
