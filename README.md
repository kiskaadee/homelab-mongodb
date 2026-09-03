# 🍃 Homelab MongoDB

Containerized MongoDB instance for local application development and document storage.

Part of the [homelab-core](https://github.com/kiskaadee/homelab-core) cluster ecosystem.

---

## 🏗️ Architecture & Storage

- **Container Image**: `mongo:latest`
- **Volume**: Named Docker volume `mongo_data` (or bind mount)
- **Network**: `proxy-net`
- **Port**: `27017`

---

## ⚙️ Environment Variables & Secrets

| Variable | Description | Source |
| :--- | :--- | :--- |
| `MONGO_ROOT_USERNAME` | Database administrator user | SOPS secrets |
| `MONGO_ROOT_PASSWORD` | Database administrator password | SOPS secrets |
| `MONGO_DOMAIN` | Internal service FQDN | `mongodb.arch-services.mywire.org` |

---

## 🚀 Deployment

### Via Orchestrator (`appctl`)
```bash
appctl up homelab-mongodb
```

### Manual Deployment
```bash
docker compose up -d
```
