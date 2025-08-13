---
title : "Create Job definition"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---


1. Go to [AWS Batch service management console]
  + Click **Job definitions**
  + Click **Create**.
![S3](/images/4.s3/CreateJobDefinitions.png)
  + At the step 1: In the name field, enter **yt-s3-copy-td**
  + In the Execution role select **ecsTaskExecutionRole**
  + CLick next
![S3](/images/4.s3/NameJobDefinitions.png)
![S3](/images/4.s3/ExecutionRole.png)
2. At the step 2 .
  + in the Job role configuration select **batch-yt-ecs-role**
  + in the vCPUs select **0.25**
  +  in the memory select **0.5GB**
  + click next
  ![S3](/images/4.s3/EnvironmentConfigurations.png)
3. At the step 3:
  + In the Log driver select **awslogs**
  + Click next
  ![S3](/images/4.s3/LoggingConfiguration.png)
4. At the step 4:
   + Click create job definition
![S3](/images/4.s3/JobDefinitionReview.png)