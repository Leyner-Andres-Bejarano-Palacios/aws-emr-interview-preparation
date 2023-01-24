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

Do you know what %%info, %lsmagic and %%help are for ?

<details><summary><b>Answer</b></summary>

 - %%info: If you have started the Spark context, you can run the %%info command to access a link to the Spark UI at any time.
 - %lsmagic: lists all currently-available magic functions.
 - %%help: lists currently-available Spark-related magic functions provided by the Sparkmagic package

</details>

<details><summary><b>Source</b></summary>

- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-studio-debug.html
- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-studio-magics.html

</details>

### Theorical Question 3

How would you change the config to compress the output of spark job ?

<details><summary><b>Answer</b></summary>

-jobconf mapred.output.compress=true

</details>

<details><summary><b>Source</b></summary>

- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-output-compression.html

</details>

### Theorical Question 4

How would you snappy inside of EMR ?

<details><summary><b>Answer</b></summary>

I would need to use the Amazon EMR AMIs version 2.0 and later 

</details>

<details><summary><b>Source</b></summary>

- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-output-compression.html

</details>

### Theorical Question 5

Do you understand what active and stand-by NameNode means ?

<details><summary><b>Answer</b></summary>

In an Amazon EMR cluster, two or more separate nodes are configured as NameNodes. One NameNode is in an active state and the others are in a standby state. If the node with active NameNode fails, Amazon EMR starts an automatic HDFS failover process. A node with standby NameNode becomes active and takes over all client operations in the cluster. Amazon EMR replaces the failed node with a new one, which then rejoins as a standby.

</details>

<details><summary><b>Source</b></summary>

- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-ha-applications.html

</details>

### Theorical Question 6

Do you know how could you execute spark using docker ?

<details><summary><b>Answer</b></summary>

Amazon EMR 6.x clusters are configured by default to allow YARN applications, such as Spark, to run using Docker containers. To customize your container configuration, edit the Docker support options defined in the yarn-site.xml and container-executor.cfg files available in the /etc/hadoop/conf directory. 

</details>

<details><summary><b>Source</b></summary>

- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-docker.html
- https://hadoop.apache.org/docs/r3.1.0/hadoop-yarn/hadoop-yarn-site/DockerContainers.html

</details>

### Theorical Question 7

Do you know why you maybe should not use docker for running your spark application ?

<details><summary><b>Answer</b></summary>

security concerns

</details>

<details><summary><b>Source</b></summary>

https://hadoop.apache.org/docs/r3.1.0/hadoop-yarn/hadoop-yarn-site/DockerContainers.html

</details>
