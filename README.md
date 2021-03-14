## Amazon Redshift lake house workshop

This GitHub project provides a series of lab exercises which help users get started using the Amazon Redshift as 
a consumption platform for a lake house architecture.

It leverages great content from multiple locations, but mainly thanks to the content in [https://redshift-deepdive.workshop.aws/](https://redshift-deepdive.workshop.aws/).

### Lab Setup

![Architecture Overview: A data lake architecture on 
Amazon S3 as storage, 
AWS Glue service family as data preparation tool, 
Amazon Redshift as analytics platform, 
and Amazon QuickSight or other tools as business intelligence](./assets/WorkshopOverview.png)


* Amazon S3 as storage for our data lake
* AWS Glue service family as data preparation tool
* Amazon Redshift, will be created as analytics platform
* Amazon QuickSight or other tools as business intelligence

### Amazon Redshift Clients

#### Amazon Redshift Query Editor
Redshift query editor currently only runs one SQL statement at a time. 
So, either highlight the statement you’d like to execute, 
or maintain only a single statement in each query tab at a time.

#### Amazon Redshift SQL clients

You can connect to Amazon Redshift clusters from SQL client tools over 
Java Database Connectivity (JDBC) and Open Database Connectivity (ODBC) connections. 
Amazon Redshift doesn't provide or install any SQL client tools or libraries. 
To use these tools or libraries to work with data in your clusters, 
install them on your client computer or Amazon EC2 instance. 
You can use most SQL client tools that support JDBC or ODBC drivers. 

For more information please check 
[the following guide](https://docs.aws.amazon.com/redshift/latest/mgmt/connecting-to-cluster.html)

Additionally, you can check [dbeaver](https://dbeaver.com/download/lite/) as an SQL Client.

### Windows RDP Client

If you'll use Qlik connection to Redshift lab, please make sure you have Remote Desktop client tooling. 
For more information please check the 
[documentation](https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/clients/remote-desktop-clients)

## Labs

Below are the labs that you can complete as part of this workshop. Every lab will contain 

|# |Lab Name |Lab Description |
|---- |---- | ----|
|1 |[Getting Started](lab1-getting-started/README.md) | introduction and logging into your console |
|2 |[Data Preparation Labs](lab2-data-preparation/README.md) | Prepare and load data into your Redshift cluster. Table creation, data load, and table maintenance|
|3 |[Lake house Labs](lab3-lake-house/README.md) | Connect the data you just loaded in your Redshift cluster with the rest of your data in your data lake. Query petabytes of data in your data warehouse and exabytes of data in your S3 data lake, using Redshift Spectrum |
|4 |[Data Visualization Labs](lab4-data-visualization/README.md) | Visualize your data and connect your Redshift cluster with various analytical tools. Connect directly to Amazon Quicksight or use your own BI tool such as Qlik. |
|5 |[Administration and Performance Tuning Labs](lab5-advanced-operations/README.md) | Check ways you can turn additional knobs to tune your cluster for the maximum performance efficiency given your query patterns. |
|6 |[Wrap up and Cleaning](lab6-cleaning/README.md) | Remove unneeded resources |
|7 |[Additional Resources](lab7-additional-resource/README.md) | More information on Redshift |


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This workshop templates and samples is licensed under the MIT-0 License. See the [LICENSE file](./LICENSE).
