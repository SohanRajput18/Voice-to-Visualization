# 🗣️ Voice-to-Visualization

Voice-to-Visualization is a GenAI-powered system that transforms spoken queries into real-time, interactive data visualizations. It eliminates the need for technical knowledge by enabling users to access and understand data through natural language. Designed to support multilingual voice commands, the platform helps decision-makers retrieve insights quickly and efficiently.

---

## Table of Contents  
- [Introduction](#introduction)  
- [Screenshots](#screenshots)  
- [Functional Requirements](#functional-requirements)  
- [Non-Functional Requirements](#non-functional-requirements)  
- [System Design & Implementation](#system-design--implementation)  
  - [Architecture Overview](#architecture-overview)  
- [Technology Stack](#technology-stack)  
- [Database Description](#database-description)  
- [Module Description](#module-description)  
- [Services](#services)  
- [Results and Discussions](#results-and-discussions)  
- [Testing](#testing)  
- [Conclusion & Future Scope](#conclusion--future-scope)  

---

## 📘 Introduction

This system addresses the challenge faced by production industry professionals in making timely decisions due to complex, inaccessible, or outdated data. The platform simplifies data retrieval by converting **voice commands** into **SQL queries**, fetching relevant data, and visualizing it in real-time using interactive charts and tables.

---

## ✅ Functional Requirements

- 🎤 Voice-to-Text Conversion via Google Speech-to-Text API  
- 🧠 Natural Language to SQL Mapping using SpaCy  
- 🗂️ Real-Time Data Retrieval from PostgreSQL  
- 📊 Data Visualization using Plotly.js / D3.js  
- 🔐 JWT-Based Authentication for Secure Access  
- 🌍 Multi-language and Dialect Support  

---

## 🛡️ Non-Functional Requirements

- **Accuracy:** High accuracy in speech recognition and NLP query generation  
- **Security:** Encrypted communication and access control using JWT  
- **Performance:** Response time under 3 seconds for most queries  
- **Scalability:** Handles multiple simultaneous queries efficiently  
- **Usability:** Voice-friendly, intuitive UI with accessibility features  

---

## 🏗️ System Design & Implementation

### Architecture Overview

1. User speaks a query (e.g., "Show sales from last week")  
2. Google Speech-to-Text converts voice into text  
3. Text is processed by the SpaCy NLP model to generate SQL  
4. SQL query is executed securely on PostgreSQL  
5. Data is returned and visualized in the frontend as graphs/tables

---

## 💻 Technology Stack

| Layer            | Tools/Libraries                        |
|------------------|----------------------------------------|
| **Frontend**     | React.js, Tailwind CSS, Plotly.js/D3.js |
| **Backend**      | Node.js, Express.js                    |
| **NLP**          | SpaCy (Python microservice)            |
| **Database**     | PostgreSQL                             |
| **Voice Input**  | Google Speech-to-Text API              |
| **Authentication**| JSON Web Tokens (JWT)                 |
| **Deployment**   | Render / Vercel                        |

---

## 🧾 Database Description

Tables include:

- **Users:** Login credentials, preferences  
- **Queries:** Saved voice inputs, converted SQL  
- **Results:** Cached results for optimization  
- **Logs:** Query usage history for analytics  

---

## 🧩 Module Description

- **Voice Module:** Records and sends voice input to Speech-to-Text  
- **NLP Module:** Maps text to SQL using SpaCy  
- **Query Module:** Executes queries securely  
- **Visualization Module:** Displays results as graphs/tables  
- **Auth Module:** JWT-based secure login system  

---

## 🔧 Services

- **POST /api/voice:** Accepts audio input and transcribes to text  
- **POST /api/nlp:** Converts text to SQL query  
- **GET /api/data:** Executes SQL and returns results  
- **POST /api/login /api/register:** User authentication routes  
- **GET /api/visualize:** Returns chart data for frontend  

---

## 📊 Results and Discussions

- Enabled **non-technical users** to interact with data  
- Reduced time spent on manual report generation  
- Improved data interpretation using real-time visuals  
- Smooth multi-language processing for inclusivity  

---

## ✅ Testing

Tested for:

- Voice-to-text accuracy (Google API)  
- NLP output and SQL generation (SpaCy)  
- SQL injection and secure DB access  
- Chart rendering for large datasets  
- User authentication and role-based access  

---

## 🧠 Conclusion & Future Scope

### Conclusion  
Voice-to-Visualization provides a seamless and intelligent way to interact with databases. By leveraging voice and natural language, the system democratizes data access for everyone in an organization.

### Future Scope

- 📈 Integration with ML models for predictive analytics  
- 🔌 External tool integrations (e.g., Salesforce, QuickBooks)  
- 📱 Mobile app version with offline mode  
- 🌐 Support for more regional languages and dialects  
- 🧠 AI-driven suggestions and anomaly detection  

---

## 📄 License

This project is licensed under [MIT](LICENSE).

