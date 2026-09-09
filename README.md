# AWS Cloud Resume

## Project Overview

I built this project to get hands-on experience with AWS and learn how to host and deploy a website using cloud services.

The website is a simple online resume hosted on **Amazon S3** and delivered through **Amazon CloudFront**. I also added a visitor counter using **Amazon API Gateway**, **AWS Lambda**, and **Amazon DynamoDB**.

I used GitHub to manage my project files and documentation.

## Architecture

The basic architecture of my project looks like this:

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


                    Visitor Counter
                           |
                           v
                   Amazon API Gateway
                           |
                           v
                      AWS Lambda
                        (Python)
                           |
                           v
                    Amazon DynamoDB
```

## AWS Services I Used

### Amazon S3

I used Amazon S3 to store the files for my resume website, including my HTML, CSS, JavaScript, and image files.

### Amazon CloudFront

I used Amazon CloudFront to deliver my website over HTTPS and improve content delivery by using AWS's content delivery network.

### Amazon API Gateway

I used Amazon API Gateway to create the API endpoint used by my visitor counter. The JavaScript on my website sends a request to the API when the page loads.

### AWS Lambda

I used AWS Lambda with Python to handle the visitor counter requests. The Lambda function processes the request and communicates with DynamoDB to retrieve and update the visitor count.

### Amazon DynamoDB

I used Amazon DynamoDB to store the visitor count. The database allows the counter to keep track of the number of visits to my website.

## Features

* Resume website hosted on AWS
* Website files stored in Amazon S3
* CloudFront content delivery
* HTTPS access
* Serverless visitor counter
* REST API integration
* AWS Lambda backend written in Python
* DynamoDB database
* GitHub source control and documentation

## How It Works

When someone visits my website, the request goes through **Amazon CloudFront**, which delivers the website files stored in **Amazon S3**.

The visitor counter works separately from the static website. When the page loads, JavaScript sends a request to my **Amazon API Gateway** endpoint.

API Gateway sends the request to my **AWS Lambda** function. The Lambda function uses **Amazon DynamoDB** to retrieve and update the visitor count.

The updated visitor count is then returned through the API and displayed on the website.

## What I Learned

While working on this project, I gained hands-on experience with:

* Hosting a website using Amazon S3
* Setting up Amazon CloudFront
* Using HTTPS and CDN services
* Creating and working with an API using API Gateway
* Writing a backend function using Python and AWS Lambda
* Using DynamoDB to store application data
* Connecting JavaScript to an AWS API
* Understanding basic serverless architecture
* Working with AWS permissions and configuration
* Troubleshooting AWS services
* Using GitHub to manage source code and documentation

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

## Proof of Concept

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

Some improvements I would like to make to this project in the future include:

* Set up automatic deployment using CI/CD
* Learn and use Infrastructure as Code
* Add better monitoring and logging
* Continue improving the website design
* Add additional AWS security controls
* Expand the project into a larger serverless application

## Links

**Live Website:**
https://doxwnfbixueh8.cloudfront.net/

**GitHub Repository:**
https://github.com/daniyalmr99/aws-static-resume-site

## About Me

I am building my AWS and cloud skills through hands-on projects. This project was one of my first projects using AWS, and I built it to understand how different AWS services can work together to host and deliver a real application.
