# 🍃 Homelab MongoDB & Mongo Express

NoSQL document database stack with MongoDB engine and Mongo Express interactive admin dashboard.

---

## 🏗️ Architecture & Requirements

- **Proxy Network**: Attached to external `proxy-net`
- **Domain**: `mongodb.roadtotech.me`
- **Target Port**: `8081` (Mongo Express Web GUI), `27017` (MongoDB TCP)

---

## ⚙️ Configuration & Metadata (`app.yaml`)

```yaml
name: "mongodb"
aliases:
  - "mongo"
  - "db-nosql"
domain: "mongodb.roadtotech.me"
description: "MongoDB NoSQL Database & Express Admin Panel"
visible: false
auth: false
networks:
  - proxy-net
env:
  MONGO_DOMAIN: "mongodb.roadtotech.me"
```

---

## 🚀 Deployment

### Via Orchestrator (`appctl`)
```bash
appctl up mongodb
```

### Manual Deployment
```bash
docker compose up -d
```

---

## 📄 License
This repository is released into the public domain under the [Unlicense](LICENSE).
