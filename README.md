# GO-Kafka-MongoDB-Prometheus-Grafana

This project demonstrate a GO Microservice project stating:

- **Kafka** (event streaming)
- **MongoDB** (data persistence)
- **Prometheus** (metrics scraping)
- **Grafana** (visualization)
- **Kafdrop** (Kafka UI)


This project shows how to build and monitor an event-driven microservice with modern observability tools.

---

##  Tech Stack

- **Backend:** Go (Echo Framework, gRPC)
- **Messaging:** Apache Kafka
- **Database:** MongoDB
- **Monitoring:** Prometheus, Grafana, Node Exporter
- **UI:** Kafdrop (Kafka UI)
- **Containerization:** Docker & Docker Compose

---

##  Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Ujjwal226/GO-Kafka-MongoDB-Prometheus-Grafana.git
cd GO-Kafka-MongoDB-Prometheus-Grafana


2. Start the Services
docker-compose up --build -d


Check containers:

docker ps --format "table {{.Names}}\t{{.Image}}\t{{.Ports}}"

3. Health Check

curl.exe -i http://localhost:5007/health


Expected: 200 OK

Testing the Microservice


3. Create a Product
$body = @{
  categoryId  = '64e5e0c2b591a09b168e8c21'
  name        = 'Sample Product'
  description = 'A test product'
  price       = 12.99
  quantity    = 5
  rating      = 7
  imageUrl    = 'https://example.com/img.jpg'
  photos      = @('https://example.com/img1.jpg','https://example.com/img2.jpg')
} | ConvertTo-Json -Depth 5

Invoke-WebRequest -Uri 'http://localhost:5007/api/v1/products' `
  -Method Post -ContentType 'application/json' -Body $body -UseBasicParsing

Get Product by ID
Invoke-RestMethod -Uri "http://localhost:5007/api/v1/products/REAL_ID"

4. Update Product
$update = @{
  categoryId  = '64e5e0c2b591a09b168e8c21'
  name        = 'Updated Product'
  description = 'Updated description'
  price       = 20.99
  quantity    = 10
  rating      = 9
  imageUrl    = 'https://example.com/new.jpg'
  photos      = @('https://example.com/new1.jpg','https://example.com/new2.jpg')
} | ConvertTo-Json -Depth 5

Invoke-RestMethod -Uri "http://localhost:5007/api/v1/products/REAL_ID" `
  -Method Put -ContentType 'application/json' -Body $update



5. Observability & Monitoring

Kafka

Kafdrop UI: http://localhost:9000

View create-product and update-product topics.

Prometheus

Prometheus UI: http://localhost:9090

Example queries:

go_goroutines{job="products-microservice"}

go_memstats_heap_alloc_bytes{job="products-microservice"} / 1024 / 1024

Grafana

Grafana UI: http://localhost:3000

Default login: admin / admin

Add Prometheus as data source: http://prometheus:9090




Summary

This project demonstrates:

Building a Go microservice

Event streaming with Kafka

Data persistence with MongoDB

Monitoring with Prometheus & Grafana


Kafka visualization with Kafdrop