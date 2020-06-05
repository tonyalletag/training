# Key Takeaway
This 3 Day Course shows us just how Amazon is taking over the world.  Cory and I took this course in downtown Denver at Denver Place, January 24-26, 2018.  The instructor says this will get you about 60% to being able to pass the Associate Developer Certification.  Overall, good design is critical, so that even if you're not using all of the 4000 AWS services Amazon offers, portable lightweight well-designed code will make you're life easier when you do go AWS.

# Agenda 

## Day 1: Foundations of AWS

* Foundations
* Choosing your data store
* S3
* DynamoDB

## Day 2: Event-driven development
* Kinesis streams
* SWF/Step functions
* SQS & SNS
* Lambda

## Day 3: 
* Security
* Elasticache
* Automatic deployments

# Highlights 

## DAY 1

Best practices for developing Cloud apps
* Have a loosely coupled design
* Architect for resiliency
* Design for failure
* Log metrics
* Monitor performance
* Implement strong DEVOPS model
* Be aware of security and regulatory restrictions
* Add security to every layer


_Layers_

Data

Application

Guest OS

^Customer Owned

>AWS Owned 

Hypervisor

Network

Physical

IAM Identity and Access Management

ARN AWS Resource Name

Data stores
* S3 simple storage service
* store and retrieve
* scalable, reliable, fast, secure
* 3 hours downtime per year 
* price based on storage

Glacier (think deep freezer storage)
* Archived data, unlimited 
* Low cost, Pay as you pull  it out

DynamoDB the nosql database
* Document and key value pair store
* Cost based on size and performance

ElastiCache 
* In mem cache

RDS
* Relational
* AWS covers backup and patching

Redshift
* Warehousing petabytes of data

CAP theory: sacrifice one for another

* **C**onsistency
* **A**vailability
* **P**artition-tolerance

AWS data stores consistency decreased as availability increased

Exponential back off
* Allowing a exponential amount of time to recover depending on number resources

AWS allows for auto scaling
* Fixed and percentage, up and down

## DAY 2

Event driven development 

Kinesis
* Streams/event channel
* Writes 1000 rec/sec 1MB/SEC
* Reads 5TPS, 2 MB/sec
* 1Mb blob max per
Add Firehose to dump data to stores

Orchestration SWF
* Step functions now preferred to manage workflow SWF
* Consider state machines
* Edge transitions set the cost; Pay per transition
* States are task, choice, parallel, fail, success, wait

SNS simple notification service
* Pub/sub, topic, fast and simple
* 256KB max msg
* One to many

SQS simple queue service
* Persisted, not FIFO by default, guaranteed delivery
* Cost-based on millions of messages equals cents
* Fifo is 300 messages per second
* Up to 256 kilobytes Max per message
* Based on polling 0 to 20 seconds
* One to one

SNS + SQS = Fan-out pattern

Lambda
* Compute service
* Good for small process
* Doesn't require ec2 instance
* Serverless app

Use XRAY for debugging

Use Serverless Application repo for shared Lambdas

## DAY 3

Use DevSecOps
* DevOps with Security at each level

3 things to do when you get root account
* Become IAM admin
* Remove root key
* Turn on Multi-factor Auth

Use IAM Simulator to test policies

Use Cognito for mobile ID management

Use Beanstalk and CloudFormation for automatic (and fast!) deployments

# AWS resources

https://console.aws.amazon.com

https://run.qwiklabs.com

https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf

https://us-west-2-aws-training.s3.amazonaws.com/awsu-ilt/AWS-100-DEV/v2.3/binaries/studentMaterials/fullCodeForAllLabs.html

cloudcraft.co

# Next Up for Certification

* _Associate renewable every 2 years_
* _Professional renewable every 4 years_

1. Read "Well Architected White Paper"
1. Run through developer training on qwiklabs
1. Pay $20 for practice exam


