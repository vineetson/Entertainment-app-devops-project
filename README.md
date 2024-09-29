# Entertainment Web Application

## Project Overview
This project involves the development of a scalable and cost-optimized cloud architecture for an entertainment app that streams movies and TV shows to users worldwide. The infrastructure is designed to handle a large user base, ensuring efficient delivery of content with minimal operational costs.

## Problem Statement
As the cloud architect for this project, the goal was to design a scalable, high-performance cloud infrastructure capable of handling high concurrency and fluctuating traffic patterns, while remaining cost-effective. The solution had to deliver seamless streaming experiences for users across different devices.

## Solution Overview
The solution utilizes various AWS services to build a robust, scalable cloud infrastructure. It integrates media ingestion, storage, processing, and distribution components, ensuring optimal content delivery and user satisfaction. The infrastructure also leverages machine learning models to offer personalized content recommendations to users.

### Key AWS Services Used:
1. **Amazon S3**: For storing multimedia content (movies, TV shows) with intelligent-tiering for cost-optimized storage.
2. **Amazon CloudFront**: Content Delivery Network (CDN) to ensure fast and reliable delivery of content worldwide.
3. **Amazon EC2**: Hosting frontend and backend services, including authentication and business logic.
4. **AWS Elemental MediaConvert**: Video transcoding and format conversion to prepare media for streaming.
5. **Amazon DynamoDB**: Storing metadata and user preferences.
6. **Elastic Load Balancer (ELB)**: For distributing traffic across EC2 instances for high availability.
7. **AWS Lambda**: For serverless computing tasks such as media processing and data handling.
8. **Amazon CloudWatch**: Monitoring, logging, and alerting for system health.
9. **Amazon SageMaker**: Used to build machine learning models for content recommendation.
10. **Amazon API Gateway**: Managing APIs for secure and scalable communication between the client and the cloud infrastructure.

### Security Measures:
- **Amazon Cognito**: Secure user authentication and authorization.
- **Virtual Private Cloud (VPC)**: For network isolation and security, with public and private subnets.
- **IAM (Identity and Access Management)**: Managing access to AWS resources, enforcing least-privilege policies.

## Architecture Diagram
![Solution Architecture Diagram](https://github.com/vineetson/Entertainment-app-devops-project/blob/master/SA_EA_devops%20project.png?raw=true)

## Solution Workflow

### Admin Side:
1. **Authentication & Authorization**: Admins log in via AWS Cognito and access the system through a secure API gateway.
2. **Content Upload**: Media files are uploaded via Lambda to an S3 bucket and metadata is stored in DynamoDB.
3. **Content Processing**: Uploaded media is processed and transcoded using AWS Elemental MediaConvert, optimized for streaming.
4. **System Monitoring**: CloudWatch is used for monitoring resources and generating performance metrics.

### User Side:
1. **User Authentication**: Users log in via AWS Cognito for secure access.
2. **Content Discovery & Consumption**: Users stream video content via CloudFront, and receive personalized recommendations through SageMaker.
3. **Secure Payment**: Payments for subscriptions are handled securely with real-time notifications through Amazon SNS.

## Requirements
- AWS S3 for storage
- Amazon EC2 for hosting
- AWS Lambda for event-driven compute
- AWS SageMaker for recommendations
- Amazon API Gateway for API management
- CloudFront for global content delivery

## Conclusion
The project successfully delivers a scalable and cost-efficient solution for an entertainment platform, providing seamless streaming experiences and personalized recommendations. With the integration of cloud-native services and robust security measures, this architecture ensures reliability, performance, and cost optimization.
