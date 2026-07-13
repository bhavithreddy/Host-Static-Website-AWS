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
<img width="1491" height="462" alt="Screenshot 2026-07-14 023847" src="https://github.com/user-attachments/assets/f74c47d5-42dd-4fca-8be4-84b6e35ef763" />
<img width="1439" height="174" alt="Screenshot 2026-07-14 023747" src="https://github.com/user-attachments/assets/21962a92-6d1e-48cd-ab58-3871e49c87da" />
<img width="1470" height="530" alt="Screenshot 2026-07-14 023731" src="https://github.com/user-attachments/assets/2fb48204-3bb2-4707-9681-70923ed91b6c" />
<img width="1491" height="568" alt="Screenshot 2026-07-14 023719" src="https://github.com/user-attachments/assets/be615459-d32c-460a-bcd0-4fc725707566" />
<img width="681" height="157" alt="Screenshot 2026-07-14 023647" src="https://github.com/user-attachments/assets/e5bc6914-154e-4247-a8f3-83e487244194" />

---

## Author

**Bhavith Reddy**

Learning and building hands-on AWS & DevOps projects.
