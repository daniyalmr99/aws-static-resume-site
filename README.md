# AWS Cloud Resume – Serverless Web Application

## Project Overview
Built and deployed a cloud-hosted resume website using AWS. The frontend is stored in Amazon S3 and delivered through CloudFront over HTTPS. I also built a serverless visitor counter using API Gateway, AWS Lambda, and DynamoDB.

---

## Architecture Diagram

User
  │
Amazon CloudFront
  │
Amazon S3
  │
Static Resume Website

Visitor Counter:
Browser -> API Gateway -> AWS Lambda -> Amazon DynamoDB


## AWS Services Used
Amazon S3: Stores the website’s HTML, CSS, and JavaScript files. Direct public access is restricted so the site is served through CloudFront.

CloudFront

Change to:

Amazon CloudFront: Delivers the website globally over HTTPS and caches content for faster loading.

API Gateway

Change to:

Amazon API Gateway: Provides the API endpoint used by the website to request and update the visitor count.

Lambda

Change to:

AWS Lambda: Runs the Python code that processes visitor-count requests without requiring a server.

DynamoDB

This one especially sounds AI-ish right now:

Operates as a NoSQL persistent data storage layer, incrementing live visitor traffic counts.

Change it to:

Amazon DynamoDB: Stores and updates the website’s visitor count.

Much better.

⸻

 5.⁠ ⁠Change “Key Features”

I wouldn’t remove this section, but simplify it.

Replace the current bullets with:

•⁠  ⁠Global Content Delivery: Website content is delivered through Amazon CloudFront.
•⁠  ⁠HTTPS: Traffic is securely served over HTTPS.
•⁠  ⁠Serverless Backend: API Gateway, Lambda, and DynamoDB power the visitor counter without a traditional server.
•⁠  ⁠Dynamic Visitor Counter: JavaScript retrieves the visitor count from the API without reloading the page.
•⁠  ⁠Version Control: Project files and documentation are maintained with Git and GitHub.

One important correction: the current README says:

Version Control: Complete source code and resource definitions maintained in a GitHub repository.

I would remove “resource definitions” unless he actually has Infrastructure-as-Code files such as CloudFormation/Terraform/SAM/CDK in the repo. From the screenshots, I only see README.md, index.html, and the screenshot. We don’t want his README claiming something he hasn’t actually uploaded.

⸻

 6.⁠ ⁠Rewrite “What I Learned”

This is where we can make the project sound much more like Daniyal actually wrote it.

Replace that entire section with:

What I Learned

•⁠  ⁠CloudFront & S3: Learned how to host a static website in S3 and deliver it securely through CloudFront.
•⁠  ⁠Serverless APIs: Learned how API Gateway, Lambda, and DynamoDB can work together to create a backend without managing a server.
•⁠  ⁠API Integration: Connected the frontend to the backend using JavaScript fetch() requests.
•⁠  ⁠Cloud Security: Learned how to restrict direct access to the S3 bucket and serve the website through CloudFront.

And if he actually had to troubleshoot CORS, add:

•⁠  ⁠Troubleshooting: Worked through CORS issues between the frontend and API and learned how to configure the required headers.

That is excellent interview material because someone can ask him, “What problem did you run into?” and he can actually explain it.

⸻


## Proof of Concept

![Live Website Screenshot](website-screenshot.png)
*Live Cloud Resume interface displaying dynamic visitor counter metrics.*
