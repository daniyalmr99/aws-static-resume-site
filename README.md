# AWS Cloud Resume

## Project Overview

I built this project to get hands-on experience with AWS and learn how to host and deploy a website using cloud services.

The website is a simple online resume hosted on **Amazon S3** and delivered through **Amazon CloudFront**. I also added a visitor counter that uses **Amazon API Gateway** to communicate with the backend.

I used GitHub to keep track of my project files and documentation.

## Architecture

The basic setup of my project looks like this:

```text
User
  |
  v
CloudFront
  |
  v
S3
  |
  v
Static Resume Website


Visitor Counter
  |
  v
API Gateway
  |
  v
Backend
  |
  v
Database
```

## AWS Services I Used

### Amazon S3

I used S3 to store the files for my resume website, including my HTML, CSS, and JavaScript files.

### Amazon CloudFront

I used CloudFront to deliver my website and enable HTTPS. It also helps deliver the website faster by using AWS's content delivery network.

### Amazon API Gateway

I used API Gateway for the visitor counter. The JavaScript on my website sends a request to the API, which then communicates with the backend.

### Backend / Database

The visitor counter uses a backend and database connected to API Gateway.

**Backend:** `AWS Lambda (running Python)`

**Database:** `[Amazon DynamoDB]`

## Features

* Resume website hosted on AWS
* Website files stored in Amazon S3
* CloudFront for content delivery
* HTTPS access
* Visitor counter
* API integration
* GitHub repository for source code and documentation

## How It Works

When someone visits my website, the request goes through CloudFront and the website files are served from S3.

The visitor counter works separately. When the page loads, JavaScript sends a request to my API Gateway endpoint. The backend processes the request and returns the visitor count, which is then displayed on the website.

## What I Learned

While working on this project, I learned more about:

* Hosting websites with Amazon S3
* Setting up CloudFront
* HTTPS and CDN basics
* Working with API Gateway
* Connecting JavaScript to an API
* Basic serverless architecture
* AWS permissions and configuration
* Troubleshooting AWS services
* Using GitHub to manage my project

## Technologies

* HTML
* CSS
* JavaScript
* Amazon S3
* Amazon CloudFront
* Amazon API Gateway
* AWS Lambda (Python)
* Amazon DynamoDB
* GitHub

## Project Structure

```text
.
├── index.html
├── website-screenshot.png
└── README.md

## Proof of Concept

### Website

![Website Screenshot](website-screenshot.png)

## Future Improvements
### Website

![Website Screenshot](website-screenshot.png)

### Website

*Add a screenshot of my deployed resume website here.*

### AWS Setup

*Add a screenshot of my AWS configuration here.*
## Links

**Live Website:** `https://doxwnfbixueh8.cloudfront.net/`

**GitHub Repository:** `https://github.com/daniyalmr99/aws-static-resume-site`

## Future Improvements

Some things I would like to add or improve in the future:

* Set up automatic deployment using CI/CD
* Learn and use Infrastructure as Code
* Add better monitoring and logging
* Improve the design of the website
* Add more AWS security controls
* Build a larger serverless application

**GitHub Repository:** `[Add GitHub URL]`
**GitHub Repository:** `https://github.com/daniyalmr99/aws-static-resume-site`
**Live Website:** `https://doxwnfbixueh8.cloudfront.net/`

**GitHub Repository:** `[Add GitHub URL]`

## About Me

I am currently building my AWS and cloud skills through hands-on projects. This project was one of my first projects using AWS, and I built it to understand how different AWS services can work together to host and deliver a real application.
