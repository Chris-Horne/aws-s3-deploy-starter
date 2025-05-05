# AWS S3 Static Site Deployment Guide

This guide walks you through deploying a static website using:

- ✅ AWS S3 (public hosting)
- ✅ Route 53 (custom domain, optional)
- ✅ Certificate Manager (HTTPS)

---

## 📦 Step 1: Upload to S3

1. Go to [https://s3.console.aws.amazon.com](https://s3.console.aws.amazon.com)
2. Click **"Create Bucket"**
   - Uncheck "Block all public access"
   - Name your bucket (e.g. `my-portfolio-site`)
3. After it's created, upload your `index.html` file
4. Go to **Properties > Static website hosting**
   - Enable it
   - Set `index.html` as the default

---

## 🌐 Step 2: Set Up a Custom Domain (Optional)

1. Go to **Route 53**
2. Register or use a domain
3. Point the domain to your S3 bucket endpoint via an alias record

---

## 🔐 Step 3: Add HTTPS (Optional)

1. Go to **AWS Certificate Manager**
2. Request a public certificate for your domain
3. Attach it via CloudFront or use it with your domain in Route 53

---

## ✅ Done

Visit your S3 site endpoint (or custom domain) and see it live!
