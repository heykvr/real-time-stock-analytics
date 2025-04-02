# real-time-stock-analytics

# Real-Time Stock Market Analytics

## 📌 Project Overview
Real-Time Stock Market Analytics is a **distributed system** designed to handle **millions of stock market events in real time**. It collects stock prices from various sources, processes them using **Kafka** and **ClickHouse**, and provides **real-time analytics** and **alerts** using **FastAPI** and **Redis**. The system is designed for **high availability**, **fault tolerance**, and **scalability** using **Kubernetes** and **AWS Free Tier**.

## 🚀 Key Features
- **Live Stock Data Fetching** (Go + Kafka Producer)
- **Real-Time Analytics Engine** (FastAPI + ClickHouse + Kafka Consumer)
- **User Authentication & API Gateway** (FastAPI + PostgreSQL + gRPC + WebSockets)
- **Stock Price Alerts** (FastAPI + Redis)
- **Service Discovery & Communication** (Consul/Kubernetes)
- **Observability** (ELK Stack: Elasticsearch, Logstash, Kibana)
- **Monitoring & Logging** (Prometheus + Grafana + OpenTelemetry)
- **Deployment on AWS Free Tier** (EC2, RDS, S3, Kubernetes)
- **CI/CD Pipeline** (GitHub Actions + AWS)

---

## 📌 How It Works
1. **Stock-Fetcher (Go + Kafka Producer)** collects live stock prices and sends them to Kafka.
2. **Analytics Engine (FastAPI + ClickHouse)** consumes Kafka events and stores data for real-time analysis.
3. **Alerts Service (FastAPI + Redis)** checks stock price conditions and triggers alerts.
4. **API Gateway (FastAPI + gRPC + WebSockets)** routes traffic and manages user authentication.
5. **Monitoring & Logging** track system health and performance with Grafana and ELK Stack.
6. **Deployment** uses Docker, Kubernetes, and AWS Free Tier for cost-effective hosting.

---

## 📌 Project Structure
```plaintext
real-time-stock-analytics/
│── infra/               # Infrastructure (Docker, Kubernetes, Terraform)
│── services/
│   ├── stock-fetcher/   # Go service for fetching stock prices
│   ├── analytics-engine/ # FastAPI + ClickHouse for real-time analytics
│   ├── alerts-service/  # FastAPI + Redis for price alerts
│   ├── user-service/    # FastAPI + PostgreSQL for authentication
│   ├── api-gateway/     # FastAPI + gRPC + WebSockets for API gateway
│── monitoring/          # ELK Stack + Prometheus + Grafana
│── deployment/          # AWS + CI/CD pipelines
│── README.md            # Project documentation
```

---

## 📌 How to Set Up & Run the Project

### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/yourusername/real-time-stock-analytics.git
cd real-time-stock-analytics
```

### **2️⃣ Start Kafka and Zookeeper (Using Docker Compose)**
```sh
cd infra/kafka
docker-compose up -d
```
Check running containers:
```sh
docker ps
```

### **3️⃣ Start Microservices**
Run each service separately:
```sh
cd services/stock-fetcher && go run main.go
cd services/analytics-engine && uvicorn main:app --reload
cd services/alerts-service && uvicorn main:app --reload
cd services/user-service && uvicorn main:app --reload
cd services/api-gateway && uvicorn main:app --reload
```

### **4️⃣ Run Monitoring & Logging**
```sh
cd monitoring
docker-compose up -d
```

### **5️⃣ Deploy to AWS (EC2 + RDS + Kubernetes)**
```sh
cd deployment
terraform apply
```

---

## 📌 Tech Stack
| Component      | Technology  |
|---------------|------------|
| **Backend**       | Go, FastAPI |
| **Messaging**     | Kafka      |
| **Storage**       | ClickHouse, PostgreSQL |
| **Caching**       | Redis      |
| **API Gateway**   | FastAPI + gRPC + WebSockets |
| **Observability** | ELK Stack, Prometheus, Grafana |
| **Deployment**    | Docker, Kubernetes, AWS Free Tier |
| **CI/CD**        | GitHub Actions |

---

## 📌 Deployment Plan
1. **Week 1:** Setup Kafka, PostgreSQL, ClickHouse, and microservices.
2. **Week 2:** Implement inter-service communication (gRPC, WebSockets).
3. **Week 3:** Setup observability, logging, and monitoring.
4. **Week 4-5:** Deploy everything on AWS (EC2, RDS, S3, Kubernetes).
5. **Week 6:** Optimize performance, scale services, finalize documentation.

---

## 📌 Contributions
Feel free to fork the repo, open issues, or submit PRs! 🚀

