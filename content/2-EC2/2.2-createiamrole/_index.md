---
title : "Create role"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.1.2 </b> "
---

#### Create Role 

1. Go to [IAM service management console]
  + Click **Role**.
  + Click **Create role**.

![IAM](/images/2.prerequisite/IAM.png)
![IAM](/images/2.prerequisite/Create role.png)

2. At the step 1 **select trusted enity** page.
  + In the **Service or use case** select **EC2**.
  + Click **Next**.

![VPC](/images/2.prerequisite/UseCase.png)


3. At the step 2 **Add permissions**.
  + In the **Permissions policies** Click **AmazoneEC2ContainerRegistryFullAccess**.
  + Click **Next**.

![VPC](/images/2.prerequisite/PermissionsPolices.png)

4. At the step 3 **Name,review, and create**.
  + In the **Role name**  field, enter **batch-yt-role**
  + Click **Create role**

![VPC](/images/2.prerequisite/Name,review and create.png)