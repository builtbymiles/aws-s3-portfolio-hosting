# 🚀 AWS S3 Portfolio Hosting

This project documents how I hosted my personal portfolio website on **Amazon Web Services (AWS)** using **S3 Static Website Hosting**.

> Live site: [View on AWS S3](http://miles-portfolio.s3-website-us-east-1.amazonaws.com)

---

## 📁 Project Overview

I created a cloud-hosted version of my portfolio site using AWS S3. The deployment involved:
- Creating an S3 bucket with static website hosting enabled
- Uploading an HTML portfolio (`index.html`)
- Configuring bucket permissions and public access policies
- Generating a public-facing URL to access the site globally

---

## 🧰 Technologies Used

- **AWS S3** – Static file storage + hosting
- **IAM Bucket Policy** – For public file access
- **HTML/CSS** – For the portfolio layout
- **GitHub** – Version control and source storage

---

## 🔐 Permissions Configuration

To allow public access to the portfolio, I used the following bucket policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowPublicReadAccess",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::miles-portfolio/*"
    }
  ]
}
