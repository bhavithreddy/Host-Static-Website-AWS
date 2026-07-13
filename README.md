# Static Website Hosting on AWS using S3 and CloudFront

This project demonstrates how to host a static website on AWS using Amazon S3 and Amazon CloudFront. The website is stored in a private S3 bucket and served securely through CloudFront over HTTPS using Origin Access Control (OAC).

The goal of this project was to understand how AWS services work together to deliver a secure and scalable static website.

---

## Architecture

```
User
   │
   ▼
CloudFront (CDN)
   │
   ▼
Private S3 Bucket
```

---

## AWS Services Used

- Amazon S3
- Amazon CloudFront
- IAM
- AWS CLI

---

## Features

- Static website hosting
- Private S3 bucket
- HTTPS enabled through CloudFront
- Origin Access Control (OAC)
- Custom error page
- CloudFront cache invalidation using AWS CLI

---

## Project Structure

```
.
├── index.html
├── error.html
└── assets/
```

---

## Steps Performed

- Created a private S3 bucket
- Uploaded website files
- Created a CloudFront distribution
- Configured Origin Access Control (OAC)
- Set the default root object
- Added custom error pages
- Tested the website using the CloudFront URL
- Updated the website using AWS CLI and invalidated the CloudFront cache

---

## Commands Used

Upload website files

```bash
aws s3 sync ./website s3://<bucket-name>
```

Invalidate CloudFront cache

```bash
aws cloudfront create-invalidation \
  --distribution-id <distribution-id> \
  --paths "/*"
```

---

## What I Learned

- Hosting static websites on Amazon S3
- Using CloudFront as a CDN
- Securing S3 with Origin Access Control
- Managing cache invalidation
- Basic IAM best practices
- Deploying website updates using AWS CLI

---

## Future Improvements

- Add a custom domain using Route 53
- Configure SSL with ACM
- Automate deployment using GitHub Actions
- Provision the infrastructure using Terraform

---

## Author

**Bhavith Reddy**

Learning and building hands-on AWS & DevOps projects.
