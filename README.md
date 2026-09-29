# AWS Serverless Three-Tier Application
 
## Overview
Designed and implemented a fully serverless three-tier web architecture using AWS managed services to provide centralized email storage accessible by multiple users.
 
## Architecture
<img width="807" height="436" alt="Serverless Architecture Diagram" src="https://github.com/user-attachments/assets/495e9c1e-ad39-4529-b388-ec0c9684bc2e" />
screenshots/Serverless-Architecture-Diagram.png

## AWS Services Used
- Amazon S3
- Amazon CloudFront
- Amazon API Gateway
- Amazon DynamoDB
- AWS IAM
 
## Design Decisions
The architecture intentionally removes AWS Lambda and uses API Gateway Velocity Template Language (VTL) mapping templates to write directly to DynamoDB.

Benefits:
- Reduced latency
- Lower operational overhead
- Reduced cost
- Fewer managed components
- Automatic scaling
 
## Architecture Flow
1. User accesses application through CloudFront.
2. CloudFront retrieves static website content from Amazon S3.
3. User submits an email record using the web form.
4. API Gateway receives the request.
5. VTL Mapping Templates transform the payload.
6. DynamoDB stores the email record.
 
## Security
- Least-privilege IAM policies
- HTTPS delivery through CloudFront
- AWS-managed service security controls
 
## Role
Architect & Developer
Designed, implemented, secured, tested, and documented the complete solution.
