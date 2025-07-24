# 🌀 Serverless Spring Boot REST API (Java 21 + AWS Lambda + API Gateway)

A serverless REST API built using **Spring Boot 3** and deployed as an **AWS Lambda function** behind an **API Gateway**. This project demonstrates how to run a modern Spring Boot app in a fully serverless architecture without managing any servers.

---

## 🚀 Project Overview

This project adapts a Spring Boot 3 application using **Spring Cloud Function** so it can run inside AWS Lambda. The API is exposed to the internet via **API Gateway**, making it suitable for stateless, cost-efficient backend services.

---

## ⚙️ Tech Stack

- Java 21
- Spring Boot 3
- Spring Cloud Function
- AWS Lambda
- API Gateway
- Maven
- (Optional) AWS SAM for deployment

---

## 🧠 How the Project Works

> A **client** (like a browser, Postman, or frontend app) sends HTTP requests to **API Gateway**, which forwards the request to an **AWS Lambda function** running the **Spring Boot** application. The function handles the request and sends back a response via API Gateway.

### 🔄 Request Flow:

```

Client → API Gateway → AWS Lambda (Spring Boot) → Response

````

---

## 📦 API Endpoints (Example)

| Method | Endpoint         | Description               |
|--------|------------------|---------------------------|
| GET    | `/courses`       | Fetch list of courses     |
| POST   | `/courses`       | Add a new course          |
| PUT    | `/courses/{id}`  | Update a course by ID     |
| DELETE | `/courses/{id}`  | Delete a course by ID     |



---

## 📁 Project Structure

```bash
serverless-spring-api/
├── src/
│   └── main/java/
│       └── com/example/serverless/
│           ├── handler/                # Lambda function handlers
│           ├── model/                  # Data models (DTOs)
│           ├── service/                # Business logic (optional)
│           ├── config/                 # AWS-related config
│           └── ServerlessApplication.java  # Spring Boot main class
│
├── pom.xml                   # Maven dependencies and build setup
├── template.yaml             # AWS SAM template (if using SAM)
├── README.md                 # Project documentation
````

---

## 🧪 Run Locally

You can test the Spring Boot app locally (optional):

```bash
mvn spring-boot:run
```

---

## 🚀 Deployment Options

### Option 1: Manual Upload via AWS Console

1. Package the project:

   ```bash
   mvn clean package
   ```
2. Go to AWS Lambda console, create a new function (Java 21), and upload the JAR.
3. Set the handler as:

   ```
   org.springframework.cloud.function.adapter.aws.FunctionInvoker::handleRequest
   ```

### Option 2: Deploy Using AWS SAM (Recommended)

1. Install AWS CLI & AWS SAM CLI
2. Build & deploy:

   ```bash
   sam build
   sam deploy --guided
   ```

---

## 📊 Logs & Monitoring

Use AWS CloudWatch to view logs:

```bash
aws logs tail /aws/lambda/<your-function-name> --follow
```

---

## 👨‍💻 Author

**Nireeksh**
Java Backend Developer | Cloud & DevOps Enthusiast
[GitHub](https://github.com/nireekshshetty)
