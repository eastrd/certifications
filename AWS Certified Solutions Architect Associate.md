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
- **Connect**: It is a Contact-Center-As-A-Service, think of it like having your own call center in the cloud. It enables you to configure service & have dynamic personal / natural customer engagement in scale.
- **Simple Email Service**: A great way of sending large amounts of emails. Highly customisable..
<br>

###### Business Productivity
- **Alexa for Business**: Can be used to dial into a meeting room / inform IT that the printers are broken / Order ink for the printers...
- **Chime**: It is like Google Hangout / Zoom Meeting. It is used for video conferencing. It can record the meeting and is very accurate, even with low bandwidth.
- **Work Docs**: Similar to DropBox but for AWS...
- **WorkMail**: Similar to Office365...
<br>

###### Desktop & App Streaming
- **Workspaces**: VDI solution - Running an actual OS on the AWS cloud that streams down to the device. 
- **AppStream 2.0**: Similarily runs an app on the cloud but streams down to device. Similar to Citrix...
<br>

###### IoT
- **iOT**: ...
- **iOT Device Management**: Managing many of devices at scale...
- **Amazon FreeRTOS**: Completely free... An OS for microcontroller.
- **Greengrass**: A software that runs local compute, messaging, sync, data caching, ML interface capabilities for connected devices in a secure way., 
<br>

###### Game Development
- **GameLift**: A service that helps you to develop games including VR games...
<br>

--------

### Examinable Sections
- AWS Global Infrastructure
- Compute
- Storage
- Databases
- Migration
- Networking & Content Delivery
- Management Tools
- Analytics
- Security & Identity & Compliance
- Application Integration
- Desktop & App Streaming

---------

#### AWS Global Infrastructure
- 16 regions in the world, 44 availability zones (Dec 2017)
- 6 more regions & 17 more availability zones (2018)
- **AWS will NOT test you on specific numbers, nor the number of AZ or Regions!**
- Region: Geographical area (e.g. Sydney, London). Each region consists of 2 or more AZ (availability zones).
- AZ: Simply data centers each with redundant power, networking and connectivity. Two AZ can be in the same region, but they are far apart in the case of disasters so the data can be protected.
- Edge Locations: Endpoints for AWS used for caching contents. (consists CloudFront, AWS CDNs). More edge locations (currently 96) than regions.
- **Exam Tips:** Understand the difference between a region, AZ, and an edge location.

-------

#### Identity Access Management (IAM)

###### Terminologiy:
- Users: End Users.
- Groups: A collection of users under one set of permissions.
- Roles: You create roles and can then assign them to AWS resources.
- Policies: A document that defines one (or more permissions). You apply policy documents on top of Users/Groups/Roles. (JSON format)

###### What is IAM?
- IAM allows you to manage users and their level of access to the AWS console. It is important to understand IAM and how it works, both for the exam and for administrating a company's AWS account in real life.

###### What does IAM give you?
- Centralised control of your AWS account.
- Shared access to your AWS account.
- Granular permissions.
- Identity federation (including Active Directory, Facebook, LinkedIn etc).
- Multifactor authentication.
- Provide temporary access for users/devices and services where necessary.
- Allows you to set up your own password rotation policy.
- Integrates with many different AWS services.
- Supports PCI DSS compliance.

###### IAM Details
- IAM is **Global** because users, groups, roles, policies are globally available.
- Best practise for AWS is to create a root account and uses it to create an account with assigned permissions. Root account is only to be logged in once or twice when needed to.
- After creating the users, the Access key and Secret Access key are for AWS APIs and you are **only going to see them once**, if you lose it you will have to create another pair...
- New users have no permissions when first created.
- Always set up multifactor auth on root account!
- You can create & customise password rotation policies.


-------------
#### S3

###### Basics
- S3 stands for "Simple Storage Service".
- Secure, Durable, Scalable object storage.
- Upload files: 0B - 5TB. Unlimited storage, price is calculated by space occupied...
- Buckets have a universal name space.
- Bucket url rules: e.g. https://s3-eu-west-1.amazonaws.com/eastrd
- When you upload a file to S3, you will receive a HTTP 200 if upload is successful.
- Optional encryptions: Client side / Server side:
   - Amazon S3 Managed Keys (SSE-S3).
   - KMS (SSE-KMS).
   - Customer Provided Keys (SSE-C).
- Control access to buckets using bucket ACL / Policies.
- By default, all buckets are **private** and all objects stored inside them are **private**.

###### Data Consistency Model
- **Read after Write consistency** for PUTS of new objects.
- **Eventual Consistency** for overwrite PUTS and DELETES (can take some time to propagate, i.e. The content could still be the old ones in some time).

###### Key-Value Store
- Key (Name of the object)
- Value (the data that's made up by a sequence of bytes)
- Version ID (important for versioning)
- Metadata 
- Subresources:
  - Access Control Lists (individual permissions on files)
  - Torrents

###### S3 Basics
- Built & Guaranteed for 99.99% availability.
- Amazon guarantees 99.999999999% durability for S3 information (11 9's)
- Tiered storage available. (different storage classes).
- Lifecycle management (Similar to log rotation).
- Version control on files.
- Encryptions.
- Secure your data using Access Control List (individual files) or Bucket policies (bucket level).

###### Storage Tiers / Classes
- S3 Standard: 99.99% availability, 99.99999999% durability, stored redundently across multiple devices in multiple facilities, and is designed to sustain the loss of 2 facilities concurrently.
- S3 IA: "Infrequent Accessed" - For data that is accessed less frequently, but requires rapid access when needed. Lower fee than S3, but you are charged a retrieval fee. Just like S3 Standard, it is stored across multiple facilities and multiple devices.
- S3, One Zone, IA: Lower cost option for infrequent accessed data, but do not require the multiple Availability Zone data resilience. (**1 AZ Only**)
- Glacier: Cheapest storage, for data archieval only: Expedidited (restored within few mins), Standard, Bulk(5-12h). A Standard retrieval takes 3-5 hours.
- Lowest cost + Don't care about retrieval times: Glacier.
- Low cost + Care about retrieval times: IA.
- Don't care cost + Durable: S3 Standard.

###### Charges
- Storage (/GB)
- Number of Requests
- Storage Management Pricing (~tags, i.e. Metadata)
- Data Transfer Pricing (Transferring data from one region to another: Cross-Region-Replication)
- Transfer Acceleration (Uses CloudFront: Edge locations ~CDNs)

###### Version Control
- Stores all version of an object (including all writes and even if you delete an object - places a "Delete Marker" on the file, need to delete the version in order to "truly" delete)
- Great backup tool, but not ideal if there are frequent changes to big files.
- Once enabled, Versioning cannot be disabled, only suspended.
- Integrates with Lifecycle rules.
- Versioning's MFA Delete capcability can be used to provide additional layer of security.

###### Cross Region Replication (CRR)
- Versioning must be enabled on both **source** and **destination** buckets.
- Regions must be unique, you cannot replicate buckets in the same region.
- Files in an existing bucket are not replicated, but can be copied using AWS cli. All subsequent files will be replicated automatically.
- You cannot replicate to mutliple buckets or use daisy chaining.
- Delete markers are replicated, but deletion aren't replicated.

###### Lifecycle Management
- Can be used in conjunction with versioning.
- Can be applied to **current** and **previous** versions.
- Actions can be done:
  - Transition to Standard - IA storage class (Minimum 30 days after creation date)
  - Archive to Glacier storage class (30 days after IA, if relevant).
  - Permantly delete.

###### Security & Encryption
- Two types of encryption:
   - In Transit:
      - SSL / TLS
   - At Rest:
      - Server Side Encryption
	     - S3 Managed Keys - SSE-S3
		 - AWS Key Management Service, Managed Keys - SSE-KMS
		 - Customer Provided Keys - SSE-C
	  - Client Side Encryption


##### READ S3 FAQ BEFORE EXAM


----------

#### CloudFront

###### What is a CDN ("Content Delivery Network")
-  A system of distributed servers (network) that delivers resources to a user based on the geographical locations of the user, orign of the resource and the CDN server.
- Terminology:
   - Edge locations: Where resources are cached.
   - Origin: This is the origin of all files that the CDN will distribute. It can be an S3 bucket, an EC2 instance, an Elastic Load Balancer (with EC2 instances behind it) or Route53.
   - Distribution: Name given to the CDN which consistes of a collection of Edge Locations.
   - Web Distribution: Typically used for Websites.
   - RTMP: Used for Media Streaming.

###### How does CloudFront work
- It can be used to deliver your resource (static, dynamic, streaming and interactive) using a global network of edge locations.
- Requests for resource are automatically routed to the nearest edge location for optimal performance.
- AWS CloudFront is optimized to work with other AWS services, but would also work for non-AWS origin resources.
- Edge locations are not just READ only, it can be written too.
- Objects are cached for the life of TTL.
- You can clear cached objects, but you will be charged... ("Invalidation")
- You can restrict viewer access to CloudFront CDNs using **Signed URLs** or **Signed Cookies**.

###### 