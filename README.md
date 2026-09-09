# AWS Cloud Resume – Serverless Web Application

## Project Overview
Built and deployed a responsive, cloud-hosted resume application using AWS services, featuring global HTTPS content delivery via CloudFront and a dynamic live visitor counter powered by a serverless REST API backend.

---

## Architecture Diagram
┌──────────────────┐
                 │   S3 Bucket      │
            ┌───►│ (Static Site)    │
            │    └──────────────────┘
[ User Browser ]┤
│    ┌──────────────────┐     ┌─────────────────┐     ┌─────────────────┐
└───►│ CloudFront CDN   │────►│ API Gateway     │────►│ AWS Lambda      │────► [ DynamoDB ]
│ (HTTPS / Edge)   │     │ (REST Endpoint) │     │ (Python Engine) │      (Visitor DB)
└──────────────────┘     └─────────────────┘     └─────────────────┘

## AWS Services Used
* **Amazon S3**: Hosts static website assets (HTML5, CSS3, JavaScript) with public web access restricted to CloudFront Origin Access Control.
* **Amazon CloudFront**: Serves content over HTTPS with global edge caching and low latency.
* **Amazon API Gateway**: Exposes a CORS-enabled HTTP REST API endpoint (`GET /count`) to receive fetch calls from the frontend script.
* **AWS Lambda**: Executes a serverless Python backend function to process incoming visitor count logic.
* **Amazon DynamoDB**: Operates as a NoSQL persistent data storage layer, incrementing live visitor traffic counts.

---

## Key Features
* **Global Content Delivery**: Optimized static asset delivery with global edge-location caching.
* **Secure Delivery**: Enforced HTTPS encryption using CloudFront SSL/TLS certificates.
* **Dynamic Serverless Integration**: Asynchronous JavaScript API calls directly update the site view count without full page refreshes.
* **Version Control**: Complete source code and resource definitions maintained in a GitHub repository.

---
## What I Learned
* **Cloud Security**: Configured CORS headers and SSL/TLS HTTPS delivery for web traffic.
* **Content Delivery Networks**: Understood edge location caching, TTL behaviors, and origin configurations in CloudFront.
* **Asynchronous Web Fetching**: Integrated client-side REST API calls with serverless backends using modern JavaScript (`fetch`).

---

## Proof of Concept

![Live Website Screenshot](website-screenshot.png)
*Live Cloud Resume interface displaying dynamic visitor counter metrics.*
