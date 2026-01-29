# TalkSpace : Mental Health Care System

## 📝 Project Overview
TalkSpace is a digital health platform that can provide mental health consultations either through chat with a doctor or TalkBot integrated with Artificial Intelligence

## 🎯 Problem Statement & Solution

#### Problem Statement
Access to mental health services is often constrained by limited availability of professionals, high consultation costs, and social stigma. These challenges make it difficult for users to seek timely and consistent mental health support, especially through conventional face-to-face services.

#### Solution
TalkSpace delivers a web-based digital mental health platform that enables online consultations with verified doctors and an AI-powered chatbot (TalkBot).
The platform allows users to:
- Consult with doctors through real-time chat
- Interact with TalkBot for mental health guidance and emotional support
- Access services in a private and secure environment
- Receive affordable and flexible mental health support

By integrating real-time communication, scalable services, and AI-powered assistance, TalkSpace helps reduce access barriers and supports users throughout their mental health journey.

## ✨ Features
| Feature                            | Description                                                                                                  |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| User Management                    | Allows users to register, authenticate, and manage their profiles                                            |
| Doctor Management                  | Enables verified doctors to register, log in, manage profiles, and update availability status                |
| Admin Management                   | Provides administrative control for managing system users and monitoring platform operations                 |
| Online Consultation                | Supports real-time mental health consultations between users and doctors using real-time communication       |
| TalkBot (AI Chatbot)               | AI-powered chatbot integrated with a GPT-based model to provide mental health guidance and emotional support |
| Premium Subscription               | Allows users to request premium access with expiration management                                            |
| OTP-Based Password Recovery        | Implements secure OTP verification for password reset and recovery                                           |

## 🚀 Tools and Technologies

* Go Programming Language
* Echo Go Framework
* GORM for Object Relational Mapping
* PostgreSQL for Relational Database
* Redis for Caching
* Elasticsearch & Kibana for Search and Monitoring
* WebSocket for Real-Time Communication
* JSON Web Token (JWT) for Authentication
* Docker for Containerization
* CI/CD Pipeline using GitHub Actions
* Amazon Web Services (AWS)
  * Amazon Elastic Compute Cloud (EC2)
  * Amazon Relational Database Service (RDS)
  * Amazon ElastiCache
  * Amazon OpenSearch Service
* Large Language Model (LLM) with Generative Pre-trained Transformer (GPT)
* Prompt Engineering for AI ChatBot Integration
* Postman for API Testing

## 🏛️ System Design and Architecture

* Clean Architecture
* Hexagonal Architecture
* Domain-Driven Design (DDD)
* Command Query Responsibility Segregation (CQRS)
* Microservices Architecture
* REST API
* WebSocket-Based Communication

## 📚 Documentation
* [TalkSpace Manual Book](https://www.linkedin.com/in/fildzaanf/overlay/Project/171912786/treasury?profileId=ACoAACUWZU0BVkHMbX1M4LCrukocRWtG4D9vXHw)

## 📡 API Endpoints

#### Users

* Account

| Method | Endpoint                  | Description       |
| ------ | ------------------------- | ----------------- |
| POST   | `/users/account/register` | Register new user |
| POST   | `/users/account/login`    | Login user        |

* Password
  
| Method | Endpoint                          | Description                      |
| ------ | --------------------------------- | -------------------------------- |
| POST   | `/users/password/forgot-password` | Request password reset           |
| POST   | `/users/password/verify-otp`      | Verify OTP                       |
| PATCH  | `/users/password/new-password`    | Set new password (Authenticated) |
| PATCH  | `/users/password/change-password` | Change password (Authenticated)  |

* Profile
  
| Method | Endpoint                  | Description         |
| ------ | ------------------------- | ------------------- |
| GET    | `/users/profile/:user_id` | Get user profile    |
| PUT    | `/users/profile/:user_id` | Update user profile |

* Premium
  
| Method | Endpoint                                          | Description               |
| ------ | ------------------------------------------------- | ------------------------- |
| POST   | `/users/premium/request-premium/:request_premium` | Request premium access    |
| PATCH  | `/users/premium/update-expired`                   | Update premium expiration |
| GET    | `/users/premium`                                  | Get premium request users |

#### Doctors
* Account

| Method | Endpoint                    | Description     |
| ------ | --------------------------- | --------------- |
| POST   | `/doctors/account/register` | Register doctor |
| POST   | `/doctors/account/login`    | Login doctor    |

* Password

| Method | Endpoint                            | Description                      |
| ------ | ----------------------------------- | -------------------------------- |
| POST   | `/doctors/password/forgot-password` | Request password reset           |
| POST   | `/doctors/password/verify-otp`      | Verify OTP                       |
| PATCH  | `/doctors/password/new-password`    | Set new password (Authenticated) |
| PATCH  | `/doctors/password/change-password` | Change password (Authenticated)  |

* Profile
  
| Method | Endpoint                      | Description           |
| ------ | ----------------------------- | --------------------- |
| GET    | `/doctors/profile/:doctor_id` | Get doctor profile    |
| PUT    | `/doctors/profile/:doctor_id` | Update doctor profile |

* Status
  
| Method | Endpoint                     | Description                |
| ------ | ---------------------------- | -------------------------- |
| PUT    | `/doctors/status/:doctor_id` | Update doctor availability |
| GET    | `/doctors`                   | Get all doctors            |

#### Admins
* Account
  
| Method | Endpoint                   | Description    |
| ------ | -------------------------- | -------------- |
| POST   | `/admins/account/register` | Register admin |
| POST   | `/admins/account/login`    | Login admin    |

* Password
  
| Method | Endpoint                           | Description                      |
| ------ | ---------------------------------- | -------------------------------- |
| POST   | `/admins/password/forgot-password` | Request password reset           |
| POST   | `/admins/password/verify-otp`      | Verify OTP                       |
| PATCH  | `/admins/password/new-password`    | Set new password (Authenticated) |
| PATCH  | `/admins/password/change-password` | Change password (Authenticated)  |

* Profile
  
| Method | Endpoint                    | Description       |
| ------ | --------------------------- | ----------------- |
| GET    | `/admins/profile/:admin_id` | Get admin profile |

#### TalkBot

| Method | Endpoint   | Description            |
| ------ | ---------- | ---------------------- |
| POST   | `/talkbot` | Create TalkBot message |

#### Consultation 

| Method | Endpoint                                 | Description              |
| ------ | ---------------------------------------- | ------------------------ |
| POST   | `/consultations/createRoom`              | Create consultation room |
| GET    | `/consultations/joinRoom/:roomId/:token` | Join consultation room   |
| GET    | `/consultations/getRooms`                | Get active rooms         |
| GET    | `/consultations/getDoctors`              | Get available doctors    |



