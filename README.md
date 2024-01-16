# IAM Section

## Users
Mapped to physical users with AWS Console access through passwords.

## Groups
Collections of users for streamlined permissions management.

## Policies
JSON documents defining permissions for users or groups.

## Roles
Assigned to EC2 instances or AWS services for specific permissions.

## Security
Multi-Factor Authentication (MFA) and Password Policies for enhanced security.

## AWS CLI
Command-line interface to manage AWS services efficiently.

# EC2 Section

## EC2 Instance
AMI (OS) + Instance Size (CPU + RAM) + Storage + security groups + EC2 User Data.

## Security Groups
Firewall attached to the EC2 instance.

## EC2 User Data
Script launched at the first start of an instance.

## SSH
Start a terminal into our EC2 Instances (port 22).

## EC2 Instance Role
Link to IAM roles.

## Purchasing Options
On-Demand, Spot, Reserved (Standard + Convertible), Dedicated Host, Dedicated Instance.

## AWS SDK
Programming language interface for managing AWS services programmatically.

## Access Keys
Credentials for accessing AWS services via CLI or SDK.

## Audit
Utilize IAM Credential Reports and IAM Access Advisor for comprehensive auditing.

# EC2 instance storage

# ELB & ASG

## High Availability vs Scalability vs Elasticity vs Agility in the Cloud

## Elastic Load Balancers (ELB)
Distribute traffic across backend EC2 instances, can be Multi-AZ. Supports health checks. 4 types: Classic, Application, Network, Gateway.

## Auto Scaling Groups (ASG)
Implement Elasticity for your application, across multiple AZ. Scale EC2 instances based on demand, replace unhealthy. Integrated with ELB.

# Amazon S3

## Buckets vs Objects
Global unique name, tied to a region.

## S3 security
IAM policy, S3 Bucket Policy (public access), S3 Encryption.

## S3 Websites
Host a static website on Amazon S3.

## S3 Versioning
Multiple versions for files, prevent accidental deletes.

## S3 Replication
Same-region or cross-region, must enable versioning.

## S3 Storage Classes
Standard, IA, IZ-IA, Intelligent, Glacier (Instant, Flexible, Deep).

## Snow Family
Import data onto S3 through a physical device, edge computing.

## OpsHub
Desktop application to manage Snow Family devices.

## Storage Gateway
Hybrid solution to extend on-premises storage to S3.

# Databases & Analytics

## Relational Databases - OLTP
RDS & Aurora (SQL).

## Differences between Multi-AZ, Read Replicas, Multi-Region

## In-memory Database
ElastiCache.

## Key/Value Database
DynamoDB (serverless) & DAX (cache for DynamoDB).

## Warehouse - OLAP
Redshift (SQL).

## Hadoop Cluster
EMR.

## Athena
Query data on Amazon S3 (serverless & SQL).

## QuickSight
Dashboards on your data (serverless).

## DocumentDB
"Aurora for MongoDB" (JSON - NoSQL database).

## Amazon QLDB
Financial Transactions Ledger (immutable journal, cryptographically verifiable).

## Amazon Managed Blockchain
Managed Hyperledger Fabric & Ethereum blockchains.

## Glue
Managed ETL (Extract Transform Load) and Data Catalog service.

## Database Migration
DMS.

## Neptune
Graph database.

# Other Compute

## Docker
Container technology to run applications.

## ECS
Run Docker containers on EC2 instances.

## Fargate
Run Docker containers without provisioning the infrastructure. Serverless offering (no EC2 instances).

## ECR
Private Docker Images Repository.

## Batch
Run batch jobs on AWS across managed EC2 instances.

## Lightsail
Predictable & low pricing for simple application & DB stacks.

# Lambda

## Serverless, Function as a Service, seamless scaling, reactive.

## Lambda Billing
By the time run x by the RAM provisioned. By the number of invocations.

## Language Support
Many programming languages except Docker.

## Invocation time
Up to 15 minutes.

## Use cases
Create Thumbnails for images uploaded onto S3. Run a Serverless cron job.

## API Gateway
Expose Lambda functions as HTTP API.

# Deployment

## CloudFormation (AWS only)
Infrastructure as Code, works with almost all AWS resources. Repeat across Regions & Accounts.

## Beanstalk (AWS only)
Platform as a Service (PaaS), limited to certain programming languages or Docker. Deploy code consistently with a known architecture.

## CodeDeploy (hybrid)
Deploy & upgrade any application onto servers.

## Systems Manager (hybrid)
Patch, configure, and run commands at scale.

# Developer Services

## CodeCommit
Store code in private git repository (version controlled).

## CodeBuild
Build & test code in AWS.

## CodeDeploy
Deploy code onto servers.

## CodePipeline
Orchestration of pipeline (from code to build to deploy).

## CodeArtifact
Store software packages/dependencies on AWS.

## CodeStar
Unified view for allowing developers to do CICD and code.

## Cloud9
Cloud IDE (Integrated Development Environment) with collab.

## AWS CDK
Define your cloud infrastructure using a programming language.

# Global Applications in AWS

## Global Accelerator
Improve global application availability and performance using the AWS global network.

## AWS Outposts
Deploy Outposts Racks in your own Data Centers to extend AWS services.

## AWS WaveLength
Bring AWS services to the edge of the 5G networks. Ultra-low latency applications.

## AWS Local Zones
Bring AWS resources (compute, database, storage, ...) closer to your users. Good for latency-sensitive applications.

# Integration Section

## SQS
Queue service in AWS. Multiple Producers, messages are kept up to 14 days. Multiple Consumers share the read and delete messages when done. Used to decouple applications in AWS.

## SNS
Notification service in AWS. Subscribers: Email, Lambda, SQS, HTTP, Mobile... Multiple Subscribers, send all messages to all of them. No message retention.

## Kinesis
Real-time data streaming, persistence, and analysis.

## Amazon MQ
Managed message broker for ActiveMQ and RabbitMQ in the cloud (MQTT, AMQP... protocols).

# Monitoring Summary

## CloudWatch
- Metrics: monitor the performance of AWS services and billing metrics.
- Alarms: automate notification, perform EC2 action, notify to SNS based on metric.
- Logs: collect log files from EC2 instances, servers, Lambda functions...
- Events (or EventBridge): react to events in AWS, or trigger a rule on a schedule.

## CloudTrail
Audit API calls made within your AWS account.

## CloudTrail Insights
Automated analysis of your CloudTrail Events.

## X-Ray
Trace requests made through your distributed applications.

## AWS Health Dashboard
Status of all AWS services across all regions.

## AWS Account Health Dashboard
AWS events that impact your infrastructure.

## Amazon CodeGuru
Automated code reviews and application performance recommendations.

# VPC Closing Comments

## VPC
Virtual Private Cloud.

## Subnets
Tied to an AZ, network partition of the VPC.

## Internet Gateway
At the VPC level, provide Internet Access.

## NAT Gateway / Instances
Give internet access to private subnets.

## NACL
Stateless
