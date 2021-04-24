# Static Website on AWS

## Introduction

The cloud is perfect for hosting static websites - sites that only include
HTML, CSS, and JavaScript files - and require no server-side processing.

This project has two major intentions to implement:

  - Hosting a static site on S3
  - Accessing cached website pages using the CloudFront content delivery network (CDN)
    - CloudFront offers low latency and high transfer speeds during website rendering
    - Further, CloudFront works with public and private buckets

## Work Flow

  1. Create a public S3 bucket and upload website files to it
  2. Configure the bucket for website hosting and secure it using IAM policies
  3. Speed up content delivery using AWS's CDN service, CloudFront
  4. Access site in browser using unique CloudFront endpoint

## Dependencies

### Cloud Services

  - AWS S3 &mdash; resource hosting and deployment
  - AWS CloudFront &mdash; CDN for SPA
  - AWS EKS &mdash; Backend API
  - AWS DynamoDB &mdash; Persistent datastore
  - AWS Cognito &mdash; User authentication

### Performance Tracking and DevOps Tools

  - AWS CloudWatch &mdash; Performance and Health checks
  - Sentry &mdash; Bug reporting
    - Alternate: TBD
  - Google Analytics &mdash; Usage reporting
    - Alternate: Mixpanel
  - Travis (CI/CD)

### Frameworks

  - Ionic (Javascript - Frontend)
  - Node.js (Javascript - Backend)
