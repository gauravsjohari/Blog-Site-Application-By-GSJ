📘 Blog Site Application — Microservices Based Blogging Platform

A production-ready Blog Site Application built using Java, Spring Boot, Microservices, Domain Driven Design (DDD), CQRS, Docker, Kubernetes, and Angular/React for the frontend. This project demonstrates real-world backend engineering, scalable architecture, and cloud deployment using AWS services like Elastic Beanstalk, RDS, and S3.

⭐ Project Highlights

🔐 JWT Authentication & user management

📝 Blog creation, update, delete, search

🔍 CQRS-based Search Service for high performance

🧱 Clean DDD structure (Domain, Application, Infrastructure layers)

🐳 Dockerized microservices

☁ AWS-ready deployment architecture

📦 Modular & scalable microservices

🧪 Built for real-world backend interview demonstration

blog-site-application-by-gsj/
│── user-service/
│── blog-service/
│── category-service/
│── search-service/            # CQRS service
│── api-gateway/               # Optional
│── frontend/                  # React/Angular
│── docker/
│── kubernetes/
│── documentation/
└── README.md

🧱 Architecture Overview
🏗 Microservices Included
Service	Responsibility
User Service	Registration, login, JWT authentication
Blog Service	CRUD blog operations
Category Service	Managing blog categories
Search Service (CQRS)	Optimized read/search operations
API Gateway	Central routing (optional)

🧠 Domain Driven Design (DDD)

The backend follows DDD with:

Domain Layer: entities, aggregates, value objects

Application Layer: service interfaces, commands, queries

Infrastructure Layer: controllers, repositories, DB adapters

This ensures clean separation and scalability.

🔄 CQRS (Command Query Responsibility Segregation)

The application uses:

Write side → Blog Service (Create/Update/Delete)

Read side → Search Service (Optimized GET queries)

This dramatically improves scalability for high-traffic blog platforms.

📝 Features
👤 User Features

Register new users

Login using JWT

Role-based access (Admin/User)

📝 Blog Features

Create blog posts

Edit or delete blog posts

List all posts

Search by:

Category

Keyword

Blog duration (Recent, Weekly, Monthly)

🗂 Category Management

Create categories

Assign categories to blogs

🔍 Advanced Search (CQRS)

Fast text-based search

Filters for various blog types

🛠 Tech Stack
Backend

Java 17+

Spring Boot (Web, Security, Data JPA)

Hibernate/JPA

Docker

Kubernetes (K8s)

Lombok

Database

MySQL (Production)

MongoDB (Optional for Search)

Frontend

Angular or React

Build & Deployment

Maven

Docker Compose

Kubernetes Manifests

AWS Cloud

Elastic Beanstalk → Deploy backend

Amazon RDS → MySQL DB

S3 → Host frontend + images

API Gateway + Lambda (optional extensions)

Cognito (optional authentication alternative)

☁ AWS Deployment Architecture (Recommended)
Frontend (React/Angular) → Hosted on S3 + CloudFront

        |
        v

API Gateway → Points to Elastic Beanstalk (Microservices)

        |
        v

Microservices (Blog, User, Category, Search) → EB EC2

        |
        v

Amazon RDS (MySQL)

🏁 How to Run the Application Locally
1️⃣ Clone the Repository
git clone https://github.com/<your-username>/blog-site-application-by-gsj.git
cd blog-site-application-by-gsj

2️⃣ Start All Microservices Using Docker Compose
docker compose up --build

3️⃣ Run Each Service Individually (Optional)

Navigate to any service:

cd user-service
mvn spring-boot:run

📡 API Documentation
User Service
Method	Endpoint	Description
POST	/api/users/register	Register a new user
POST	/api/users/login	Authenticate user
Blog Service
Method	Endpoint	Description
POST	/api/blogs	Create blog
GET	/api/blogs	List all blogs
PUT	/api/blogs/{id}	Update blog
DELETE	/api/blogs/{id}	Delete blog
Category Service
Method	Endpoint	Description
POST	/api/categories	Create category
GET	/api/categories	List categories
Search Service (CQRS)
Method	Endpoint	Description
GET	/api/search?query={keyword}	Search blogs
GET	/api/search/recent	Recent blogs
GET	/api/search/category/{cat}	Filter by category
🧪 Running Tests
mvn test

🧊 Docker Build Commands
Build individual service:
docker build -t blog-user-service ./user-service

Run:
docker run -p 8081:8081 blog-user-service

☸ Kubernetes Deployment

Apply manifests:

kubectl apply -f kubernetes/


Check status:

kubectl get pods

📸 Screenshots (Add Here)

You can later upload:

Login page

Blog list page

Create blog page

Architecture diagram

📄 Documentation

Inside documentation/:

ER diagrams

Sequence diagrams

Architecture overview

API design spec

🧑‍💻 Author

Gaurav Johari
💼 Java Developer | Microservices | Spring Boot | AWS 
🏆 Coral Award Winner
