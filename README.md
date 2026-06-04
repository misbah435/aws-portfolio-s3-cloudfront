# AWS Portfolio Site — S3 + CloudFront

Personal portfolio site deployed on AWS using S3 for static hosting and CloudFront as a global CDN with HTTPS.

## Live Site
https://d1nw114jge288e.cloudfront.net

## Architecture
Browser → CloudFront (CDN + HTTPS) → S3 (static file storage)

## AWS Services Used
- **S3** — Static website hosting, file storage
- **CloudFront** — Global CDN, HTTPS termination
- **ACM** — SSL/TLS certificate
- **IAM** — User permissions and access keys
- **AWS CLI** — Bucket creation, file sync, distribution setup

## What I Built
- Created S3 bucket with static website hosting enabled
- Configured public bucket policy for file access
- Set up CloudFront distribution pointing to S3 origin
- Enabled HTTPS via AWS Certificate Manager
- Deployed and synced files using AWS CLI

## Deployment Steps
1. Create S3 bucket
   `aws s3 mb s3://misbah-portfolio-2025 --region ap-south-1`
2. Upload files
   `aws s3 sync . s3://misbah-portfolio-2025`
3. Add bucket policy for public access
4. Enable static website hosting
5. Create CloudFront distribution
   `aws cloudfront create-distribution --origin-domain-name ...`

## Cost
~$0/month — fully within AWS Free Tier
