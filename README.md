# Static Portfolio Website on AWS

## Overview
Deployed a production-ready static portfolio website using AWS with a secure, scalable, and cost-optimized architecture.

## Architecture
User → Route 53 → CloudFront → S3 (private)

## Services Used
- Amazon S3 (static website hosting)
- Amazon CloudFront (CDN + HTTPS)
- Amazon Route 53 (DNS management)
- AWS Certificate Manager (SSL/TLS)

## Key Features
- Custom domain integration (elevateaws.com)
- HTTPS enabled using ACM
- Global content delivery using CloudFront
- Secure S3 bucket (private) using Origin Access Control (OAC)
- Low-cost, serverless architecture

## Implementation Steps
1. Created S3 bucket and uploaded static website files
2. Configured CloudFront distribution with S3 as origin
3. Enabled Origin Access Control (OAC) for secure access
4. Requested SSL certificate via ACM and validated using DNS
5. Configured Route 53 hosted zone and updated nameservers in GoDaddy
6. Created DNS records to route domain to CloudFront
7. Set default root object (index.html) for proper routing

## Challenges Faced
- AccessDenied error due to missing OAC configuration
- Incorrect DNS record format during ACM validation
- Missing default root object causing root URL failure

## Learnings
- Difference between S3 website endpoint and REST endpoint
- Importance of CloudFront + OAC for secure architecture
- DNS propagation and record configuration in Route 53
- End-to-end deployment of a real-world AWS project

## Outcome
Successfully deployed a secure, fast, and scalable portfolio website accessible over HTTPS using a custom domain.
