# AWS Serverless Three-Tier Application

## Overview

Designed and implemented a lightweight, serverless three-tier web application using AWS managed services.

The application allows users to subscribe to monthly content through a web interface while leveraging a highly scalable and cost-effective cloud-native architecture.

## Architecture Diagram

screenshots/Serverless-Architecture-Diagram.png

## Business Problem

Traditional solutions often require dedicated servers, application hosting, and ongoing maintenance.

This project demonstrates how AWS managed services can provide a scalable, fault-tolerant, and cost-effective alternative.

## Architecture Components

### Presentation Tier

- Amazon S3
- Amazon CloudFront

Static website content is hosted in Amazon S3 and delivered through CloudFront.

### Logic Tier

- Amazon API Gateway
- Velocity Template Language (VTL)

API Gateway handles incoming requests and directly integrates with DynamoDB.

### Data Tier

- Amazon DynamoDB

DynamoDB stores subscription records and automatically scales based on demand.

## Key Design Decision

A major architectural decision was removing AWS Lambda from the solution.

Instead, API Gateway VTL mapping templates directly transform requests and write records into DynamoDB.

Benefits include:

- Lower latency
- Reduced costs
- Reduced operational overhead
- Fewer managed components

## AWS Services Used

- Amazon S3
- Amazon CloudFront
- Amazon API Gateway
- Amazon DynamoDB
- AWS IAM

## Screenshots

## Application Homepage

screenshots/homepage.png
screenshots/subscription-successful.png

## CloudFront Distribution

![CloudFront Distribution](screenshots/API Gateway Integration

## API Gateway Integration

screenshots/API-Gateway-Integration.png

## S3 Bucket

screenshots/S3-bucket.png

## DynamoDB Records

screenshots/dynamodb-items.png

## Author

Jonathan Machel

AWS Certified Solutions Architect - Associate
