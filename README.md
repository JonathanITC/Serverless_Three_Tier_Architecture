AWS Serverless Three-Tier Web Architecture
## Overview

Designed and implemented a fully serverless three-tier web application using AWS managed services to provide centralized email record storage with scalable, multi-user access.

The architecture emphasizes:

Low operational overhead
Automatic scaling
High availability
Cost efficiency
Simplified maintenance

Unlike traditional serverless designs, this solution removes AWS Lambda and leverages direct API Gateway to DynamoDB integration using Velocity Template Language (VTL) mapping templates.

Architecture
Presentation Tier
Amazon S3
Amazon CloudFront

Static website content is hosted in Amazon S3 and distributed globally through Amazon CloudFront to reduce latency and improve end-user performance.

Logic Tier
Amazon API Gateway
VTL Mapping Templates

API Gateway receives requests from the web application and transforms payloads using VTL templates before writing directly to DynamoDB.

This design removes Lambda execution overhead and reduces operating costs.

Data Tier
Amazon DynamoDB

DynamoDB serves as the highly available NoSQL backend and enables automatic scaling with low-latency reads and writes.

Security
IAM least-privilege policies
Restricted API permissions
AWS-managed service security controls
Key Design Decisions
Why remove Lambda?

Many serverless architectures introduce Lambda by default.

This project intentionally removed Lambda because:

No business logic required execution
Reduced latency
Eliminated cold starts
Lower cost
Fewer services to manage
Business Outcome

The solution modernizes centralized email storage by replacing traditional Outlook archive dependency with a cloud-native architecture.

Benefits include:

Multi-user accessibility
Improved scalability
Reduced maintenance effort
Lower infrastructure cost
Increased availability

AWS Services Used
Amazon S3
Amazon CloudFront
Amazon API Gateway
Amazon DynamoDB
AWS IAM

Role: Architect and Developer
Designed, implemented, secured, tested, and documented the complete solution.
