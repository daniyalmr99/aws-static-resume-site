# AWS Cloud Resume

## Project Overview

I built and deployed a serverless cloud resume on AWS using Amazon S3, CloudFront, API Gateway, AWS Lambda, and DynamoDB.

The static frontend is hosted in Amazon S3 and delivered securely through CloudFront. A serverless backend built with API Gateway, Python, AWS Lambda, and DynamoDB powers a live visitor counter.

This project demonstrates hands-on experience integrating multiple AWS services to build and deploy a functional cloud application.

## Architecture

The application uses a static frontend with a separate serverless backend:

```text
User
 |
 v
Amazon CloudFront
 |
 v
Amazon S3
 |
 v
Static Resume Website
 |
 | JavaScript API Request
 v
Amazon API Gateway
 |
 v
AWS Lambda (Python)
 |
 v
Amazon DynamoDB
 ```

## AWS Services I Used

### Amazon S3

I used Amazon S3 to host and store the static files for my resume website, including my HTML, CSS, JavaScript, and image assets.

### Amazon CloudFront

I used Amazon CloudFront to securely deliver the website over HTTPS and improve performance by caching content at AWS edge locations.

### Amazon API Gateway

I used Amazon API Gateway to create a REST API endpoint that connects the website to the serverless backend. When the page loads, JavaScript sends a request to the API, which triggers a Lambda function.

### AWS Lambda

I used AWS Lambda with Python to handle the visitor counter logic. The function retrieves the current count from DynamoDB, increments it, saves the updated value, and returns the new count through API. 

### Amazon DynamoDB

I used Amazon DynamoDB to persist the visitor count. Each request processed by the Lambda function updates the stored count, allowing the website to maintain an accurate total across visits.

## Features

•⁠  ⁠Static resume website hosted with Amazon S3
•⁠  ⁠Global content delivery using Amazon CloudFront
•⁠  ⁠Secure HTTPS access
•⁠  ⁠Serverless visitor counter with real-time updates
•⁠  ⁠REST API built with Amazon API Gateway
•⁠  ⁠Serverless backend using AWS Lambda and Python
•⁠  ⁠Visitor data stored in Amazon DynamoDB
•⁠  ⁠Frontend-to-backend integration using JavaScript
•⁠  ⁠Source control and project documentation with GitHub

## How It Works

When a user visits the website, Amazon CloudFront securely delivers the static content stored in Amazon S3 over HTTPS.

The visitor counter runs separately from the static website. When the page loads, JavaScript sends a request to the Amazon API Gateway endpoint.

API Gateway forwards the request to the AWS Lambda function. The Lambda function retrieves the current visitor count from the Amazon DynamoDB, increments it, and saves the updated value.

The updated visitor count is then returned through the API Gateway to the frontend, where JavaScript displays the new count on the website.

## What I Learned

Through this project, I gained hands-on experience with:

•⁠  ⁠Hosting and delivering static web content using Amazon S3 and CloudFront
•⁠  ⁠Configuring HTTPS delivery through CloudFront
•⁠  ⁠Building and integrating a REST API with Amazon API Gateway
•⁠  ⁠Writing serverless backend logic using Python and AWS Lambda
•⁠  ⁠Reading and updating application data with Amazon DynamoDB
•⁠  ⁠Connecting frontend JavaScript to a serverless AWS backend
•⁠  ⁠Configuring AWS permissions between services
•⁠  ⁠Understanding serverless application architecture
•⁠  ⁠Troubleshooting and testing AWS service integrations
•⁠  ⁠Managing source code and project documentation with GitHub

## Technologies

* HTML
* CSS
* JavaScript
* Python
* Amazon S3
* Amazon CloudFront
* Amazon API Gateway
* AWS Lambda
* Amazon DynamoDB
* GitHub

## Project Structure

```text
.
├── index.html
├── website-screenshot.png
└── README.md
```

## Deployment

### Live Website

The project is currently deployed and accessible through CloudFront.

**Live Website:**
https://doxwnfbixueh8.cloudfront.net/

### Website Screenshot

![Website Screenshot](website-screenshot.png)

## AWS Architecture

The application uses AWS services to separate the static website from the serverless backend.

```text
S3 + CloudFront
       |
       | Static Website
       v
     Browser
       |
       | API Request
       v
 API Gateway
       |
       v
 AWS Lambda
       |
       v
 DynamoDB
```

## Future Improvements
Planned improvements for this project include:

•⁠  ⁠Automate deployments using GitHub Actions (CI/CD)
•⁠  ⁠Implement Infrastructure as Code using Terraform
•⁠  ⁠Add monitoring and logging with Amazon CloudWatch
•⁠  ⁠Configure a custom domain using Amazon Route 53
•⁠  ⁠Strengthen IAM permissions and security controls
•⁠  ⁠Add automated testing
## Live Demo

**Live Website:**
https://doxwnfbixueh8.cloudfront.net/

**GitHub Repository:**
https://github.com/daniyalmr99/aws-static-resume-site

## About Me

I am developing hands-on cloud engineering experience by designing and deploying projects on AWS. This project demonstrates my ability to integrate multiple AWS services into a functional application with a static frontend and serverless backend.
