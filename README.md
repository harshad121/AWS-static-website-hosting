# 🌐 AWS S3 Static Website Hosting

This project demonstrates hosting a static website using **Amazon S3**, configuring bucket permissions, using **AWS CLI for deployments**, and managing project versions using **Git & GitHub**.

---

## 🚀 Project Overview

In this project, I deployed a static website using:

- **Amazon S3** for hosting
- **Bucket Policies** for public access
- **AWS CLI** for uploading files
- **Git** for version control
- **GitHub** as source repository

The final website is accessible publicly via the S3 website endpoint.

---

## 📁 Project Features

✔ Static website hosted on AWS S3  
✔ Public access configured through bucket policy  
✔ Version control with Git  
✔ Deployment using `aws s3 sync`  
✔ Secure IAM user with S3 permissions  
✔ Clean folder structure  
✔ Professional GitHub documentation  

---

## 🏗 Architecture Diagram
flowchart TD
    User((User)) -->|HTTP Request| S3[(Amazon S3 Static Website)]
    S3 -->|HTML/CSS/JS| User
    Git[Local Git Repository] -->|Push via AWS CLI| S3
    IAM[IAM User] -->|Access Key/Secret| AWSCLI[(AWS CLI)]
    AWSCLI --> S3


📦 Technologies Used

1)AWS S3
2)AWS IAM
3)AWS CLI
4)Git & GitHub
5)HTML / CSS
6)Git Bash

🛠 Steps to Deploy 

1️⃣ Create S3 Bucket :-

1)Disable Block Public Access
2)Enable Static Website Hosting

2️⃣ Upload HTML File :-

Example index.html included in this repository.

3️⃣ Add Bucket Policy


{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::<your-bucket-name>/*"
    }
  ]
}

4️⃣ Configure AWS CLI :-
aws configure

5️⃣ Deploy Website Using CLI :-
aws s3 sync . s3://your-bucket-name --exclude ".git/*"

🔗 GitHub Repository

👉 https://github.com/harshad121/AWS-static-website-hosting

🌍 Live Website URL

http://site-1210.s3-website-us-east-1.amazonaws.com


