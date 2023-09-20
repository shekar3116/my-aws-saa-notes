Course: https://learn.acloud.guru/course/certified-solutions-architect-associate/learn/a21a1644-a8e1-4760-a4e0-545ac1fc4c82/0a2db8f4-b24f-4cbf-9625-185c718280ee/watch
 
PDF slides:  https://acloudguru-content-attachment-production.s3-accelerate.amazonaws.com/1667575892970-1043%20PDF%20Export%202022_Part1.pdf
                     https://acloudguru-content-attachment-production.s3-accelerate.amazonaws.com/1667496840658-1043%20PDF%20Export%202022_Part2.pdf
 
Exam preparation pdf: https://acloudguru-content-attachment-production.s3-accelerate.amazonaws.com/1669220704360-1043%20AWS%20Certified%20Solutions%20Architect%20-%20Associate%20%28SAA-C03%29%20Table%20of%20Contents.pdf
 
 
 
Serverless
 
Lambda
	• Runtime - choose the lang to use to write the function.
	• Permissions - if you want make a API call using Lambda then attach a role to it.
	• Networking - Not need VPC, subnet and SG to run it, its an optional.
	• Resources - Define the amount of CPU and RAM.
	• Trigger - what to trigger the function?  You have to kick it off to run the function.
	•  Lambda Fun is having built-in logging and cloud watch.
	• Max timeout is 15mints max.
	• Max RAM 10Gigs.
 
  
	• Read it more on internet.
 
Container
	• Is a standard unit of software that packages up code and all its dependencies.
 
ECR 
	1. Elastic container registry - used to store the images

	1. Registry - to be provided to each account.
	2. Auth token
	3. Repository
	4. Repo policy
	5. image
ECS vs EKS
	• Both are Container Orchestration tools.
	• ECS is AWS provided CO tool, only works in AWS.
	• EKS - K8's are opensource CO tool, can be installed any where. AWS managed service is EKS.
 
Fargate
	• If you use Cloud instances or on-prem for spinning up containers you have to maintain the upgrades and infra.
	• It is server less computing engine for containers, that works with both ECS and EKS.
	• AWS manages and owns infra.
	 

	 
	• Fargate vs Lambda vs EC2
 
Amazon EventBridge
	• Formerly known as Event Bus.
	• Used to pass the Cloudwatch events from source to an endpoint.
	
	 
	• For example, write a lambda function to start ec2 instances if they are in stop state,  write a event bridge rule to monitor the state of ec2 instances and start the it if the state goes to stopped state and trigger the Lambda function. If you make instance off now then the event bridge rule get trigger the rule and calls the Lambda function.
	• This service is used to trigger an action based on something that happened in AWS.
 
EKS Distro - EKS-D
	• Kubernetes distribution based on Amazon EKS.
 
ECS anywhere
 

 
Amazon Aurora Serverless
	• ACU - Aurora capacity unit 
	• Used for new applications without knowing capacity, capacity panning and development testing needs.
 
AWS X-ray -
	AWS X-Ray helps developers analyze and debug production, distributed applications, such as those built using a microservices architecture. With X-Ray, you can understand how your application and its underlying services are performing to identify and troubleshoot the root cause of performance issues and errors.
	 
 
App Sync
AWS AppSync enables developers to connect their applications and services to data and events with secure, serverless and high-performing GraphQL and Pub/Sub APIs
 
 
 
 
SECURITY
 
DDoS
	• Distributed denial of service, which makes web server unavailable to the end users.
	• There are two types of attacks mainly, Syn floods and Amplification attack.
	• SYN Floods attack - In order to make a TCP connection from server to client there will be with 3 way hand shake, when sever sends SYN to client and excepts to SYN-ACK back, in this type of attack sends many SYNC request to the client to complete the number of attempts to make  fail the connection.
	• This is a Layer 4 attack at TCP level.
	• Amplification attack: not understood. 
	• Layer 7 attack -  Sending lot of GET requests to the server using botnet and making the web server busy.
 
CloudTrail
	• Records the events of all the API calls within the AWS account, with details who, when and what API.
	
	• It is used for investigation purpose.
	• It acts like a CCTV for AWS account.
	 
Shield
	• Free DDoS protection.
	• It protects only layer 3 and 4 only.
	• AWS shield advanced
		○ It provides enhanced protections to applications running ELB, cloud Front and Route53.
		○ It identifies the attacks like DDoS attacks and inform to the team.
		○ Protects higher bills.
	• Shield Advance costs $3000 per month.
 
AWS WAF
	• Web Application firewall and monitor the Https and Http traffic to Amazon CloudFront or ELB.
	• It operate at layer 7.
	• You can block the requests here based on country, IP address, values, strings…etc.
 
GuardDuty
	• It is threat detection service  that uses machine learning to continuously monitor for Malicious behavior's.
	• It monitors Cloud Trail logs, VPC Flow logs and DNS logs.
	 
Firewall Manager
	• Is a security management service in a single pane of glass, this allows you to centrally set up and manage firewall rules across multiple AWS accounts in AWS Org.
	• It acts like a enterprise firewall for org.
 
Macie
	• PII - personally Identifiable information.
	• Automated analysis of data stored in S3,  this service uses AI to identify the PII, PHI (personal Health info) and financial data and alerts  you to encrypt the buckets.
 
Amazon Inspector
	• Is an automated security assessment service that helps to improve Security and compliances of applications deployed on AWS.
	• It will priorities based on the security level, and provide detail report.
	• To use it, go to the instance and install the agent.
	 
KMS and CloudHSM
	• KMS - key management services.
	• Automated key rotation and creation.
	• CMK-  customer master key.
		○ To understand this think it is a PPK key.
	• HSM -v hardware security module.
		○ Physical computing device that safeguards and manages digital keys.
	• CloudHSM  - used to generate your own kyes and use them.
 
Secret manager - Vault
	• Is a service that securely store,s encrypts and rotate s your database creds and other secrets.
	• Encryption in transit.
	• Applications uses the manager API.
	• Rotating creds is super easy.
 
Parameter store
	• It is free.
	• Yu can store anything in the from of a plain text.
	• Upto 10k parameters.
 
Presigned URL and cookies
	• URL - if you want to give access to Someone who don't have access to the bucket can be provided by presigned URL.
	• This is a time duration access.
	
	• If you run above command it will generate a URL pass it to someone.
	 
	 
ARN - Amazon resource name
	• It is a uniquely identified resource name.
	
		 
AWS Certificate Manager
	• This allows you to create, manage and deploy public and private SSL certs for use of other AWS services.
	• No more paying for SSL certs, you will only for resources.
	• Automate the renewal of your SSL certs and automate the update.
 
AWS audit manager
	• With it you can continuously audit your AWS usage to make sure you stay compliant with industry standards and regulations.
	• It is automated service that produces reports specific to auditors for PCI compliance, GDPR and more.
	• Allow to do internal risk assessments.
 
AWS Artifact
	• It is a single source you can visit to get the compliance related info that matters to you, ex AWS security compliance reports or select online arrangements.
	• SOC, PCI reports…. More.
 
Cognito *****
	• It will provide authorization, authentication and user management for your web and mobile apps in a single service without need for custom code.
	• Users can login directly with username and password  of third part services like FB, amazon, apple id, gmail…
	
 
	• User pool - that provides sign-up and sign-in options for users of your application.
	• Identity pool - provides users access to aws resources.
	• You can use the together or separately.
	 
Amazon Detective
	• This is used to identify the root cause of potential security issues or suspicious activity.
	•  pulls data from AWS resources like VPC flow logs, CloudTrail logs, …..etc
	• It will generate the visualization reports.
 
AWS Network firewall
	• Is managed service that makes it easy to deploy physical firewall protection across your VPC's.
	• This is physical firewall in AWS Datacenter.
	• It works with network manager.
	 
Security Hub
	• Single place to view all security alerts, works across multiple cross accounts.
 
Automation
 
Cloud formation Templates- CFT
	• Is a declarative programming language, it supports either JSON or YAM formatting.
	• Creates immutable architecture.
	 
Elastic Beanstalk
	• PAAS - platform as service
	• AWS PAAS tool.
	• It will handle all your deployments, you can upload code, test it in a staging env and deploy in prod.
	• Its not serverless, in the backend it will spin up ec2 instance.
 
Systems Manager
	• Collection of tools we can use to automate.
	• It's not just for cloud.
	• I think it is like a Ansible,  chef.
	• It supports on-prem architecture.
	• It is free if you use it for AWS resources.
 
 
Caching
 
AWS caching options
	• CloudFront
	• ElasticCache
	• DAX
	• Global accelerator.
 
CloudFront 
	• Is a fast content delivery network (CDN) service which securely delivers data, videos, applications and API's to the edge locations.
	• Default to https connections.
	• Global distribution.
	• You can use it for non-AWS applications.
 
ElasticCache 
	• This are AWS database caching solutions.
	• Combination of two opensource tools,  Memcached and Redis.
	
	 
DAX (DynamoDB Accelerator)
	• In memory cache-  reduce DynamoDB response time from milliSec to MicroSec.
	• It is highly available and lives inside VPC.
 
Global Accelerator
	• Is a network service that sends your traffic through AWS's global network infra, so it can increase performance and help to deal with IP Caching.
	
	• Even if ELB fails or replaced with new one with diff IP, user don't need to save the new cache details here because of global accelerator.
	 
 
AWS Accounts and Organizations
 
Organization
	• AWS organization is free governance tool to allow to create  and manage multiple AWS accounts.
	• you can control all the accounts from a single location rather then jumping into the account.
	• Best practice to create a logging accounts.
	• Reserve instances can be shared across all accounts.
	• Service control policies
		○ This policies will be applied to all the resources within the account.
		○ This is ultimate to restrict permissions and even apply t the root account.
		○ SCP won't give you permissions but they only take you away!!
AWS RAM - Resource Access Manager
	• This is a free service used to share the AWS resources with other accounts within the organization.
	• Transit gateways, VPC subnets, license manager, Route53….. lot more.
	 
Cross-Account Role Access
	• Roles created to access resources in other account.
	• You have to change the role in order to use it.
 
Config
	• Is a inventory managing and control tool.
	• This is very best tool in AWS to see the resources and all the events of a resources.
	• You can also find the deleted resources events.
	• Query - you can query by resource type, tag and even deleted infra.
	• Enforce - Rules can be created to flag when something is going wrong.
	• Learn - 
 
Directory Service
	• Active directory
	• Managed Microsoft AD - is used to build the AD with our AWS cloud.
	• AD connector - it is used to connect to AD sitting outside of the AWS cloud.
 
Cost Explorer
	• Visualize your cloud costs.
	• Generate reports based on variety of factors including resource tags,
	• There many good filters to see the cost of AWS resources.
 
AWS Budgets
	• Allow orgs to easily plan and set expectations around clous costs.
	• This wills end the alerts to you if resources cost is reaching to budget or exceeds it.
	• You can add action policies to delete the resources to the budgets.
 
AWS Cost and Usage Reports
 
AWS Compute Optimizer
	• Analyzes config's and utilization metrics of AWS resources.
	• Disabled by default.
 
Saving plans
	• Compute savings
	• EC2 instances saving plans
	
 
Trusted Adviser
	• Is a fully managed best practice auditing tool.
	• It will scan 5 diff parts of account where you can adopt and improve best practices.
	
	• It’s a free service.
	 
 AWS Control Tower
	• Used lika a Ansible tower.
	• Can create accounts and manage accounts.
	
	 
AWS License Manager
	• Simplifies managing software licenses with diff vendors.
	• Centrally manage licenses across accounts and on-prem env.
	• Tracking and rule bases controls to utilize.
 
AWS Personal Health Dashboard

 
AWS Service Catalog
	• Allow Organizations to create and managed catalogs of approved IT services.
	• In simple words, engineers write CF templates and put them into the service catalog service, end users can search for required template and run for them.
	 
AWS Proton 
	• This service offers IAAC provisioning and deployment of architects.
 
AWS Well Architected Tool
	• This tool is for architects, CTO's…etc
	 
	 
	 
Migration
 
Snow Family
	• Is a set of secure appliances that provides petabyte-scale data collection and process sol's at the edge and migrate large scale data into and out of AWS.
	• SnowCone - 8TB storage, 4GB Memory and 3vCPU's.
	• SnowBall Edge - 48TB to 81 TB storage, Memory and CPU varies.
	• SnowMobile -  100PB of storage, 
		○ Used to move exabyte scale datacenter.
	 
Storage Gateway
	• Is a hybrid cloud storage service that helps to merge on-prem resources with the cloud.
	• It can also helps with a one-time migration or a long term pairing of architecture with AWS.
	• File Gateway -
		○ NFS or SMB mount
		○ Network file share.
		
 
	• Volume Gateway 
		○ Perfect for backup
	• Tape Gateway
		○ Puts your data in S3 Glacier
		 
AWS DataSync
	• Is an agent based solution to migrate on-prem storage to AWS.
	
	• It is good for one time migration.
	• It is used for lift and shift data and close the datacenter.
 
AWS Transfer Family
	• Allows you to move files in and out using SFTP, FTPS, or FTP.
	If you want to bring legacy app storage to cloud use it.
 
AWS Migration Hub
	• It is a single place to track the progress of your application migration.
	• It integrates with Server Migration Service (SMS) and Database Migration Service (DMS).
	• SMS - 
 
AWS Application Discovery Service
	• Used to plan and migrate the vm's to AWS.
	• Agentless and agent based
 
AWS Application Migration Service (MGN)
	• It is a lift and shift service.
	 
AWS DMS 
 
AWS SCT - Schema conversion tool
 
 
FrontEnd Web and Mobile
 
Amplify
	• Offers tools for front-end web and mobile developers to quickly build full-stack applications on AWS.
	• Amplify hosting - support single page application
	• Amplify studio -  easy authication  and authorization.
		○ Visually develop env to simple creation
		○ Ready to use
AWS Device Farm
	• Used to test applications and interacting android, IOS and web apps.
	• It uses actual phones and tabs.
	• Automated and remote access for testing
	• If you see question with testing apps on mobile device use this service.
 
Amazon Pinpoint
	• Enables you to engage with customers through a variety of different messaging channels.
	 
	 
Machine Learning
Amazon Comprehend 
	Amazon Comprehend uses natural-language processing (NLP) to help you understand the meaning and sentiment in your text. It is not used to transcribe text
	 
	From < https://practice-exam.acloud.guru/67be35b9-2276-4357-aa8a-525031d0126c/result/483f682d-66ae-4191-bfb1-21f391a4e31b> 
	 
Transcribe 
	Amazon Transcribe converts speech to text automatically. You can use this service to generate subtitles.
	 
	 
Kendra 
	• AI search service in websites and s3 buckets to analyze.
	• Improve customer interactions based on reading  reviews.
 
Textract
	• Extract text from the hand writing and data from the scanned copies.
 
Amazon Forecast
	• Forecast time-series forecasting
	• Time series data - example weather reports collection for every mint.
	• Example, IoT, Analytics..
 
Amazon Fraud Detector
	• AWS AI service that built to detect fraud in your data.
	 
Amazon Rekognition
	• It’s a face recognition service with AI.
 
Amazon SageMaker
	• Used to deploy ML tools.
	 
Amazon Translate 
	• Translate one language to another.
	• Integrate the Translate to app using API.
 
Media
 
Amazon Elastic Transcoder
	• Converts media files from original source format into versions that are optimized for various devices.
	• Ex smartphones, tablets and PC's
 
Amazon Kinesis Video Streams
	• If you need to stream media content from a large number of devices to AWS and run analytics, ML, playback and other process.
