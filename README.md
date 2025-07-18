# 🐳 Dockerized Data Stack

This project contains a full-featured local development stack with MySQL, PostgreSQL, Redis, MongoDB, Kafka, and MinIO—all containerized using Docker Compose. Each service includes a corresponding web UI for easy management and visualization.

---

## 📦 Services Overview

| Service       | Port   | UI/Tool        | Default Credentials                    |
|---------------|--------|----------------|----------------------------------------|
| MySQL         | 13306  | phpMyAdmin     | `dockerize_mysql` / `0111mvtT`         |
| PostgreSQL    | 5432   | phpPgAdmin     | `dockerize_postgres` / `0111mvtT`      |
| Redis         | 6379   | Redis UI       | `dockerize_redis` / `0111mvtT`         |
| MongoDB       | 27017  | Mongo Express  | `dockerize_mongo` / `0111mvtT`         |
| Kafka         | 9092   | Kafka UI       | No Auth                                |
| MinIO         | 9000   | Web Console    | `dockerize_minio` / `0111mvtT`         |

---

## 🚀 Getting Started
| Tool          | URL                                            |
| ------------- | ---------------------------------------------- |
| phpMyAdmin    | [http://localhost:8081](http://localhost:8081) |
| phpPgAdmin    | [http://localhost:8082](http://localhost:8082) |
| Redis UI      | [http://localhost:8083](http://localhost:8083) |
| Mongo Express | [http://localhost:8084](http://localhost:8084) |
| Kafka UI      | [http://localhost:8085](http://localhost:8085) |
| MinIO Console | [http://localhost:9001](http://localhost:9001) |

## ⚙️ Config
### Change the access permissions 
```bash
sudo chmod -R 777 directory
```
### MySQL
```bash
docker exec -it mysql bash

mysql -u root -p

GRANT ALL PRIVILEGES ON *.* TO 'dockerize_mysql'@'%' WITH GRANT OPTION;

FLUSH PRIVILEGES;
```