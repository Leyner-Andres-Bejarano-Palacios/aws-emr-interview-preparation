# aws-emr-interview-preparation
this as well as the other repos in the series "interview_preparation" are meant to work as study guide for getting better at been software and data engineer. In this one I will introduce the ambiguios section, because I am aware that more than one answer would fit.

I am also aware that emr are just a bunch of servers and the real important thing to understand is python, sql, spark, hadoop, hive, s3 and aws concepts like ec2 and security groups. I already have python, sql and spark repos (that I will continue nurturing) and I will soon have repos of the series "interview preparation for the rest".

## Ambiguous Questions Section

### Ambiguous Question 1

How would you connect to the EMR cluster (in a ssh way) ?

<details><summary><b>Answer</b></summary>

1. grant  permission to manage security groups for the VPC that the cluster is.
2. add an inbound rule that allows SSH access (TCP port 22) from the sources you want to have access. 
2. 
</details>

<details><summary><b>Source</b></summary>

- 
- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-connect-master-node.html

</details>

## Theorical Question Section

### Theorical Question 1

How does a iam policy for changing security groups looks like ?

<details><summary><b>Answer</b></summary>

check link in the source

</details>

<details><summary><b>Source</b></summary>

- https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_ec2_securitygroups-vpc.html

</details>

### Theorical Question 2

Do you know what %%info is for ?

<details><summary><b>Answer</b></summary>

If you have started the Spark context, you can run the %%info command to access a link to the Spark UI at any time.

</details>

<details><summary><b>Source</b></summary>

- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-studio-debug.html

</details>

