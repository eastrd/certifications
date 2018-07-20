#  AWS Certified Solutions Architect Associate
------------
### Overview
###### AWS Global Infrastructure:
- Consists of a bunch of different geographically distinct regions around the world. Inside regions there are at least two availability zones (AZ). An AZ is simply data center that's geographically isolated to each other in case of natural disasters such as flooding. Edge locations are way to cache data typically using CloudFront which is AWS's CDN.
<br>

###### Compute:
- **EC2**: "Elastic Compute Cloud" - Essentially a VM inside the AWS platform..
- **EC2 Container Service**: Run & manage dockers at scale.
- **Elastic Beanstalk**: For devs who don't understand AWS and just want to upload their code. This tools then goes & provision things such as autoscaling groups, ec2 instances, load balancers, etc. So all the devs have to focus on is their code. It features heavily in Developer Associate cert & Devops Associate cert but not too much in Solutions Architect Associate cert.
- **Lambda**: A platform where you can upload code to the cloud tahat runs without worrying about any underlying physical or virtual machines or systems. Lambda is used in Solutions Architect cert & Developer Associate cert.
- **Lightsail**: AWS's VPS service for people who don't want to understand anything about AWS or any underlying structures such as security groups etc. This will provision you with a server and give you a fixed IP address to login the server, either SSH or RDP and comes with a really cool management console. Basically a very watered down version of EC2...
- **Batch**: Used for batch computing in cloud, currently not covered in any AWS certifications.
<br>

###### Storage:
- **S3**: "Simple Storage Service" - object-based storage. You upload files to things called "buckets" that are in the cloud. S3 is very important for this cert.
- **EFS**: "Elastic File System" - Network attached storage. Store files on any EFS volume and mount it to any VM.
- **Glacier**: For data archival, similar to a cold storage with cheap pricing compare to normal storage.
- **Snowball**: A physical way to bring in large amounts of data into the AWS data center rather than transmitting it through broadband or wifi. It's easier to just send terabytes of data physically into data centers...
- **Storage Gateway**: Virtual appliances (e.g. VM in data center or HQ) that will replicate information back to S3. There are 4 different types of storage gateways.
<br>

###### Databases:
- **RDS**: "Relational Database Services" - MySQL / PostgreSQL / SQL Server / AWS Aurora / Oracle etc.
- **DynamoDB**: A non-relational database.
- **Elasticache**: A way of caching commonly used queries from database. (e.g. caching top 10 products in Elasticache rather than having web servers pulling from databases so to free up database servers to do other queries)
- **Redshift**: Data warehousing / Business intelligence - really complex queries (e.g. Management wants to know profit/loss of a particular item in Asia Pacific region. This of course can be done with production database but this query is going to take a lot of time. Hence it's suitable to use Redshift which is built for data warehousing).
<br>

###### Migration:
- **AWS Migration Hub**: A tracking service that allows you to track your applications as you migrate them to AWS. It also integrates other services within the Migration framework.
- **Application Discovery Service**: An automated tool not only detects what application you have, but also its dependencies. (e.g SQL server or Domain Controller ).
- **Database Migration Service**: Very easy way to migrate databases from on-premise into AWS.
- **Server Migration Service**: Very similar to Database Migration Service. It helps to migrate virtual / physical servers onto AWS cloud.
- **Snowball**: Snowball is in between Storage and Migration categories. It is used for migrating large amounts of data into the cloud. (Terabytes)
<br>

###### Networking & Content Delivery
- **VPC**: "Virtual Private Cloud" - Think of it like a virtual data center. You configure firewalls, AZ, network address ranges, network ICLs, route tables. It is complicated but very important.
- **CloudFront**: Amazon's content delivery network. CloudFront stores media and image files from far away location closer to where the user is at, so the user can access these assets from a nearby edge location instead of pulling them from far away location.
- **Route53**: Amazon's DNS service - Looking up domain name to IPv4 / IPv6 address.
- **API Gateway**: It's a way of creating your own APIs for other services to talk to. It's a big subject in Developer Associate cert and comes up in this cert.
- **Direct Connect**: It's a way of running a dedicated line from your coop office or data center into Amazon & will directly connect to your VPC. It's a big topic for this cert.
<br>

###### Developer Tools
(it never came up in any of the associate exams.. but.. good to know..)
- **CodeStar**: Getting a group of developers working together quite easily. It's a way of project managing your code. Basically you set up your code and have a continuous delivery toolchain and can release your code within minute. 
- **CodeCommit**: A place to store your code (i.e. source control service - Your own private Git repository).
- **CodeBuild**: Once you get your code ready, CodeBuild will compile that code for you or run testings against it and it will produce software packages that are ready to deploy.
- **CodeDeploy**: It automates application deployments to EC2 instances, but can also to premise instances as well as Lambda functions.
- **CodePipeline**: It's a continuous delivery service and is used to model/visualize/automate steps required to release your software.
- **X-Ray**: Used to debug & analyze serverless applications. It has request tracing, so you can go in and find root causes of issues and performance bottlenecks.
- **Cloud9**: An IDE environment in AWS console on web browser.
<br>

###### Management Tools
- **CloudWatch**: A monitoring service. It is the bread and butter of SysOps Administrator cert.
- **CloudFormation**: It is used all the time by solution architects in real life. It is **VERY IMPORTANT** in Solutions Architect Associate & Professional certs. It is a way of scripting infrastructure. It just takes all infrastructures and turns them into code. With a CloudFormation you can use templates or reuse the code to deploy all kind of infrastructures. It is super fun.
- **CloudTrail**: It logs changes to your AWS environment. It is turned on by default but only stores its records for one week. Highly recommend turning Cloud Trail on for across all new regions. (e.g If someone hacked your account and used it for crypto mining, you can figure out how and where they are using that service). **Very Important** for Security and Solutions Architect.
- **Config**: A really cool technology that monitors the configuration of your entire AWS environment. It has a pointing time snapshots so you can move the timer backwards/forwards by days/months so you can visualize your AWS environments and see how they are all configured. **Very Important**
- **OpsWorks**: Similar to ElasticBeanstalk - Uses Chef and Puppet to automate your environment. Covered in SysOps Associate cert, but a little bit in this cert.
- **Service Catalog**: A way of managing catalogs services that are for AWS, this can be from VM images, individual OSes, Software, DBs, all the way to multi-tier architectures. It currently does not feature in any associate or professional exams.
- **Systems Manager**: An interface for managing AWS resources, typically for EC2. It can be also used for patch maintance (e.g. Security patches across thousands of EC2 instances, it's easiler to use Systems Manager). It currently does not feature in any associate or professional exams, but as a system admin, you need to know it to do your job.
- **Trusted Advisor**; It gives you advises across different displines: Security, Saving money (downscaling). It is favoured in Security Associate, Cloud Practioneer, and Solutions Architect Associate, even in Pros...
- **Managed Services**: It helps you manage EC2 instances / autoscaling sort of things...
<br>

###### Media Services
(Brand new from reInvent 2017 except Elastic Transcoder)
- **Elastic Transcoder**: It takes the video and resizes it so it can be adapted onto different resolutions.
- **MediaConvert**: File based video transcoding service with broadcast grade features.
- **MediaLive**: Broadcast grade live video processing service.
- **MediaPackage**: Prepares and protects videos for delivery over internet.
- **MediaStore**: Storage service optimized for videos.
- **MediaTailor**: Allows to do targeted advertising into video streams without sacrificing broadcast grade service.
<br>

###### Machine Learning
- **SageMaker**: Easy access for devs onto deep learning. (reInvent 2017)
- **Comprehend**: It does sentiment analysis around data.
- **DeepLens**: A physical camera hardware that can live detect objects.
- **Lex**: Powers Alexa service - An AI chatbot.
- **Machine Learning**: Traditional machine learnings.
- **Polly**: Text-to-speech service that sounds human, it can choose different accents.
- **Rekognition**: It does both video and image recognitions.
- **Amazon Translate**: Similar to Google Translate, but Amazon's...
- **Amazon Transcribe**: Service that does automatic speech recognition (Speech-to-text).
<br>

###### Analytics
- **Athena**: Service that allows you to run SQL queries in S3 buckets.
- **EMR**: "Elastic MapReduce" - Processing large amount of data. **Important**
- **CloudSearch**: Search services.
- **ElasticSearch**: Search services.
- **Kinesis**: **Important** for Big data & Solutions Architect. A way to ingest large amounts of data into AWS. (e.g. Social media feeds/tweets)
- **Kinesis Video Streams**: ReInvent 2018. Ingest videos & run processing against it.
- **QuickSight**: Great BI tool and is very cheap compared to other tools.
- **Data Pipeline**: A way of moving data between different AWS services. 
- **Glue**: Used for ETL - (Extract, Transform, Load).
<br>

###### Security & Identity & Compliance
- **IAM**: "Identity Access Management" - **Important**
- **Cognito**: Authentication service for devices.
- **GuardDuty**: Monitors malicious activities on AWS account.
- **Inspector**: An agent to be installed on EC2 instances to check for vulnerabilities. It generates a severity list. - **Important**
- **Macie**: It scans S3 buckets and look for PII ("Personally Identifiable Information, e.g Addresses, TFN)
- **Certificate Manager**: You get SSL cert files for free. This tool manages SSL certificates. - **Need to understand**
- **CloudHSM**: Hardware security modules. It can be used to store ssh keys and other encryption keys. - **Important**
- **Directory Service**: A way of integrating Microsoft Active Directory with AWS services. - **Somewhat Important**
- **WAF**: "Web Application Firewall" - Application layer firewall to stop malicious web tarffic.  - **Important**
- **Shield**: Helps to prevent 24/7 DDoS attacks.
- **Artifact**: Portal for on-demand access to download AWS compliant reports (e.g. SOC) and also manages selected agreements.
<br>

###### Mobile Services
- **Mobile Hub**: A management console for mobile apps by using mobile hub SDKs to connect to AWS.
- **Pinpoint**: A way of using targeted push notifications to drive mobile engagement.
- **AWS AppSync**: Automatically upstates the data in web & mobile apps real time. It also updates data for offline users as soon as they connect.
- **Device Farm**: A way of testing apps on reallife devices. (e.g. Android, iPhones)
- **Mobile Analytics**: Analytics service for mobiles...
<br>


###### AR / VR
- **Sumerian**: Language that is used for AR/VR design. It allows you to use common set of tools to create these environments. You don't even need to understand how to code.
<br>


###### Application Integration
- **Step Functions**: A way of managing lambda functions with different steps to go through them.
- **Amazon MQ**: A way of doing message queues. (Similar to RabbitMQ)
- **SNS**: Notification service. (e.g. Billing alarm) **Important**
- **SQS**: A queue that can be used to decoupling infrastructure. **Important**
- **SWF**: "Super Workflow Service" - It creates a simple workflow job that essentially involves human actions in it. **Important**
<br>

###### Customer Engagement
<br>

###### Business Productivity
<br>

###### Desktop & App Streaming
<br>

###### IoT
<br>

###### Game Development
<br>

---------
##### AWS Global Infrastructure
- 16 regions in the world, 44 availability zones (Dec 2017)
- 6 more regions & 17 more availability zones (2018)
- **AWS will NOT test you on specific numbers, nor the number of AZ or Regions!**
- Region: Geographical area (e.g. Sydney, London). Each region consists of 2 or more AZ (availability zones).
- AZ: Simply data centers each with redundant power, networking and connectivity. Two AZ can be in the same region, but they are far apart in the case of disasters so the data can be protected.
- Edge Locations: Endpoints for AWS used for caching contents. (consists CloudFront, AWS CDNs). More edge locations (currently 96) than regions.
- **Exam Tips:** Understand the difference between a region, AZ, and an edge location.

##### Compute
##### Storage
##### Databases
##### Migration
##### Networking & Content Delivery
##### Developer Tools
##### Management Tools
##### Media Services
##### Machine Learning
##### Analytics
##### Security & Identity & Compliance
##### Mobile Services
##### AR / VR
##### Application Integration
##### Customer Engagement
##### Business Productivity
##### Desktop & App Streaming
##### IoT
##### Game Development


