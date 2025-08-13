1️⃣ Delete or Cancel Jobs
1.Go to AWS Console → AWS Batch → Jobs.

2.Select All jobs tab.

3.
-If the job is RUNNING / PENDING → Cancel job first.

-If the job is SUCCEEDED / FAILED → Optional to remove from list (no cost).

4.AWS CLI example:


aws batch cancel-job --job-id <JOB_ID> --reason "Cleanup"

2️⃣ Deregister Job Definitions
AWS won’t allow deletion if they are still in use.

1.AWS Console → AWS Batch → Job definitions.

2.Select each job definition → Deregister.

3.AWS CLI:

aws batch deregister-job-definition --job-definition <NAME:REVISION>

3️⃣ Delete Job Queues
Make sure no job definitions or compute environments are linked.

1.AWS Console → AWS Batch → Job queues.

2.Set state to DISABLED first.

3.Once disabled, Delete.

4.AWS CLI:


aws batch update-job-queue --job-queue <QUEUE_NAME> --state DISABLED
aws batch delete-job-queue --job-queue <QUEUE_NAME>

4️⃣ Delete Compute Environments
Managed CE: AWS will automatically remove EC2 instances after disabling.

1.AWS Console → AWS Batch → Compute environments.

2.Set state to DISABLED.

3.Once disabled, Delete.

4.AWS CLI:


aws batch update-compute-environment --compute-environment <CE_NAME> --state DISABLED
aws batch delete-compute-environment --compute-environment <CE_NAME>

5️⃣ Remove Additional Resources (Optional but Recommended)
-EC2 Spot Fleet / Auto Scaling Groups (if using Unmanaged CE).

-IAM Roles:
AWSBatchServiceRole
ecsInstanceRole (if created manually)
- ECR Repositories (if you created custom Docker images).
✅ Recommended Cleanup Order:

Jobs → Job Definitions → Job Queues → Compute Environments → IAM Roles / Logs / ECR

