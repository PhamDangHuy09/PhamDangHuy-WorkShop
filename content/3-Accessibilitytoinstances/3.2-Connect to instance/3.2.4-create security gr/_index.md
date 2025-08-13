---
title : "Create Security Group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.2.3 </b> "
---



1. Go to [EC2 service management console]
  + Click **EC2 Dashboard**.
  + Click **Security Groups**
  + Click **Create Security Groups**.

![Connect](/images/3.connect/EC2.png)
![Connect](/images/3.connect/CreateSecurity.png)

1. At the Create security group
  + in the Security group name field, enter**batch-compute-sg**
  + in the description field, enter **SG for Batch service**
  + Click **Create security group**
![Connect](/images/3.connect/BasicDesign.png)

1. Go to [IAM service management console]
   + At the Role page
   + CLick Create Role
![Connect](/images/3.connect/CreateRole.png)
   + At the step 1: In the Use Case select **Elastic Container Service Task** and click next
![Connect](/images/3.connect/Add permissions.png)
   + At the step 2: in the permissions policies select **AmazonS3FullAccess** and click next
![Connect](/images/3.connect/BasicDesign.png)
   + At the step 3: in the Role name field, enter **batch-yt-ecs-role** and click create role.
![Connect](/images/3.connect/RoleDetails.png)