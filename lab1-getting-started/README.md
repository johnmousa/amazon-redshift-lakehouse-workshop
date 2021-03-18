## 1. AWS Console Login
If you want to setup the workshop environment by yourself, goto [Setup workshop environment](#Setup-workshop-environment-by-yourself)

Follow below instructions if you attend an AWS hosted workshop or immersion day event.

### AWS account login

Please use Chrome or Firefox browser to ensure smooth lab experience.

1. Use workshop access link provided by moderator
   
   ![Click on access](https://redshift-deepdive.workshop.aws/images/gettingstarted/workshoplogin.png)
1. A hash code will be assigned to you, enter it in the text box, Click proceed
   
   ![hash code entry](https://redshift-deepdive.workshop.aws/images/gettingstarted/dashboard-hash.png)
1. Click on: “AWS Console”
   
   ![AWS console button guide](https://redshift-deepdive.workshop.aws/images/gettingstarted/dashboard-console.png)
1. Click on: “Open Console”
   
   ![Open console guide](https://redshift-deepdive.workshop.aws/images/gettingstarted/dashboard-console-login.png)
1. In the upper-right corner of the AWS Management Console, confirm you are in the desired AWS region (e.g., N. Virginia)
   
   ![Region Selection](https://redshift-deepdive.workshop.aws/images/gettingstarted/awsregion-console.png)

### Launch prerequisites template

To launch this Cloudformation template and configure security automatically using cloud formation, use the following link.
Launch

[![Launch Stack](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=RedshiftLakeHouseWS&templateURL=https://raw.githubusercontent.com/johnmousa/amazon-redshift-lakehouse-workshop/main/lab1-getting-started/stacks/amazon-redshift-lakehouse-ws.yaml)

### Template Parameters

The AWS CloudFormation stack will be launched in N. Virginia (us-east-1) region to enable this lab setup. 
The stack has deployed the following resources.

* Dedicated VPC Setup (VPC/Subnet/Gateway/etc.)
* Amazon Redshift cluster
* AWS Glue database and 4 crawlers
  * 2 crawlers will be used to speed up the labs by crawling already prepared data
  * The other 2 will be used to crawl data that you will prepare in your S3 bucket
* Amazon S3 bucket

1. Click on services, type cloudformation and select CloudFormation.
   
   ![Navigate to AWS CloudFormation Service](https://redshift-deepdive.workshop.aws/images/gettingstarted/cloudformation-services-1.png)
1. Click on the stack name 
   
   ![Select the stack](https://redshift-deepdive.workshop.aws/images/gettingstarted/cloudformation-stack-2.png)
1. Click on output
   
   ![Check the outputs](https://redshift-deepdive.workshop.aws/images/gettingstarted/cloudformation-stackoutput.png)

#### Capture parameters and values

Capture the following key/value pairs in the Output. Make note of them in textpad or notepad, You will use these values in the labs.

|Key 	|Description|
|---- |---- |
|RedshiftClusterRoleArn 	|Amazon Redshift cluster IAM role. This role will be used to create external schema, copy, and unload commands.|
|RedshiftClusterUser 	|Amazon Redshift cluster user|
|RedshiftClusterPassword 	|Amazon Redshift cluster user password|
|ClusterEndpoint 	|Amazon Redshift cluster endpoint|
|PSQLConnection     |Connection command to cluster from your Cloud9 environment|
|TaskDataBucketName 	|Amazon S3 bucket name, this will be referenced in the unload command in the lab.|
|GlueExternalDatabaseName 	|AWS Glue database name, this will be referenced in the creation of external schema|

### Next step
Continue to [Preparing data to be loaded Redshift cluster](../lab2-data-preparation/README.md).