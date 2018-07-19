# AWS Certified Solutions Architect Associate
------------
### Overview
###### AWS Global Infrastructure:
- Consists of a bunch of different geographically distinct regions around the world. Inside regions there are at least two availability zones (AZ). An AZ is simply data center that's geographically isolated to each other in case of natural disasters such as flooding. Edge locations are way to cache data typically using CloudFront which is AWS's CDN.

###### Compute:
- **EC2**: "Elastic Compute Cloud" - Essentially a VM inside the AWS platform..
- **EC2 Container Service**: Run & manage dockers at scale.
- **Elastic Beanstalk**: For devs who don't understand AWS and just want to upload their code. This tools then goes & provision things such as autoscaling groups, ec2 instances, load balancers, etc. So all the devs have to focus on is their code. It features heavily in Developer Associate cert & Devops Associate cert but not too much in Solutions Architect Associate cert.
- **Lambda**: A platform where you can upload code to the cloud tahat runs without worrying about any underlying physical or virtual machines or systems. Lambda is used in Solutions Architect cert & Developer Associate cert.
- **Lightsail**: AWS's VPS service for people who don't want to understand anything about AWS or any underlying structures such as security groups etc. This will provision you with a server and give you a fixed IP address to login the server, either SSH or RDP and comes with a really cool management console. Basically a very watered down version of EC2...
- **Batch**: Used for batch computing in cloud, currently not covered in any AWS certifications.

###### Storage:
- **S3**: "Simple Storage Service" - object-based storage. You upload files to things called "buckets" that are in the cloud. S3 is very important for this cert.
- **EFS**: "Elastic File System" - Network attached storage. Store files on any EFS volume and mount it to any VM.
- **Glacier**: For data archival, similar to a cold storage with cheap pricing compare to normal storage.
- **Snowball**: A physical way to bring in large amounts of data into the AWS data center rather than transmitting it through broadband or wifi. It's easier to just send terabytes of data physically into data centers...
- **Storage Gateway**: Virtual appliances (e.g. VM in data center or HQ) that will replicate information back to S3. There are 4 different types of storage gateways.

##### Databases:
- **RDS**: "Relational Database Services" - MySQL / PostgreSQL / SQL Server / AWS Aurora / Oracle etc.
- **DynamoDB**: A non-relational database.
- **Elasticache**: A way of caching commonly used queries from database. (e.g. caching top 10 products in Elasticache rather than having web servers pulling from databases so to free up database servers to do other queries)
- **Redshift**: Data warehousing / Business intelligence - really complex queries (e.g. Management wants to know profit/loss of a particular item in Asia Pacific region. This of course can be done with production database but this query is going to take a lot of time. Hence it's suitable to use Redshift which is built for data warehousing).

##### Migration:
- 




##### AWS Global Infrastructure
- 16 regions in the world, 44 availability zones (Dec 2017)
- 6 more regions & 17 more availability zones (2018)
- **AWS will NOT test you on specific numbers, nor the number of AZ or Regions!**
- Region: Geographical area (e.g. Sydney, London). Each region consists of 2 or more AZ (availability zones).
- AZ: Simply data centers each with redundant power, networking and connectivity. Two AZ can be in the same region, but they are far apart in the case of disasters so the data can be protected.
- Edge Locations: Endpoints for AWS used for caching contents. (consists CloudFront, AWS CDNs). More edge locations (currently 96) than regions.
- **Exam Tips:** Understand the difference between a region, AZ, and an edge location.

##### Compute
- 

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
##### Media Services
##### AR / VR
##### Application Integration
##### Customer Engagement
##### Business Productivity
##### Desktop & App Streaming
##### IoT
##### Game Development


