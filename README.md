# Serverless Spring Boot REST API with AWS Lambda & API Gateway

This project showcases a **serverless REST API** built using **Spring Boot 3 (Java 21)** and deployed as an **AWS Lambda function** behind an **API Gateway**. It demonstrates how a Spring Boot application can be adapted to run serverlessly on AWS using **Spring Cloud Function**.

---

##  Project Overview

- Java 21 + Spring Boot 3
- Serverless execution using AWS Lambda
- API Gateway for exposing RESTful endpoints
- Spring Cloud Function to adapt Spring Boot for Lambda
- Infrastructure as Code using AWS SAM (optional)
- No external database used (data is mocked/in-memory)

---

##  Tech Stack

- Java 21
- Spring Boot 3
- Spring Cloud Function
- AWS Lambda
- API Gateway
- Maven
- AWS SAM CLI (optional for deployment)

---


## Flow 

Client → API Gateway → Lambda (Spring Boot) → Returns response

