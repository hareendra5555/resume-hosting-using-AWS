# resume-hosting-using-AWS
This project demonstrates how to host a static resume website on AWS using S3, CloudFront, Route 53, and AWS Certificate Manager (ACM) for SSL/TLS encryption.

# AWS S3, CloudFront, Route 53, and ACM Resume Website

This project demonstrates how to host a static resume website on AWS using **S3**, **CloudFront**, **Route 53**, and **AWS Certificate Manager (ACM)** for SSL/TLS encryption. The website is accessible via a custom domain (`therealhareendra.com`) with secure HTTPS delivery.

---

## Project Overview

The goal of this project is to host a static resume website on AWS with the following features:

- **S3 Bucket**: Used to store and serve the static website files (HTML, CSS, etc.).
- **CloudFront**: Provides content delivery with low latency and high transfer speeds. It also ensures secure delivery using HTTPS.
- **Route 53**: Manages DNS routing to map the custom domain `therealhareendra.com` to the CloudFront distribution.
- **AWS Certificate Manager (ACM)**: Generates and manages the SSL/TLS certificate for secure HTTPS connections.

The website is accessible via `https://therealhareendra.com`.

---

## Technologies Used

- **AWS S3**: For hosting static website files.
- **AWS CloudFront**: For content delivery and caching.
- **AWS Route 53**: For DNS management.
- **AWS Certificate Manager (ACM)**: For SSL/TLS certificate management.
- **HTML/CSS**: For the website's front-end.

---

## Steps to Deploy

### 1. **Create an S3 Bucket**
   - Create an S3 bucket named `therealhareendra.com` and configure it for static website hosting.
   - Upload the website files (`detailed-resume.html`, `style.css`, `error.html`) to the bucket.
   - Apply the bucket policy to allow public read access.

  

### 2. **Set Up CloudFront**
Create a CloudFront distribution with the S3 bucket as the origin.

Configure the distribution to use the custom domain therealhareendra.com.

Enable HTTPS by attaching the SSL/TLS certificate from ACM.

### 3. **Configure Route 53**
Create a hosted zone for therealhareendra.com.

Add an alias record that points to the CloudFront distribution.

### 4. **Generate SSL/TLS Certificate with ACM**
Request a public certificate for therealhareendra.com using ACM.

Validate the certificate using DNS validation.

### 5. **Deploy the Website**
Once everything is set up, the website will be accessible via https://customdomain.com.
