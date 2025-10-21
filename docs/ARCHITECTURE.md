# System Architecture (v1.1)

Open-WebUI ←→ FastAPI Backend ←→ AI Core
│
▼
Data & History Engine
│
▼
Strategy + Risk Manager
│
▼
Notifications / Logs

yaml
Copy code

### Layer Overview

| Layer | Components | Purpose |
|-------|-------------|----------|
| **Data Layer** | ETL, Cache, Feed Connectors | Ingest and clean data |
| **AI Analysis** | Pattern-recognition models | Detect repeating sequences |
| **Strategy Engine** | ML + Rule logic | Generate bias and trade signals |
| **Risk Manager** | Backtesting, exposure limits | Portfolio safety |
| **Notification** | Discord / Telegram bots | Deliver alerts |
| **Visual Console** | Open-WebUI plugin | Charts and admin control |

### Open-WebUI Integration

Open-WebUI is the primary visual interface.  
A custom plugin provides an additional right-hand “Trading Dashboard” panel.

**API Endpoints**

| Endpoint | Function |
|-----------|-----------|
| `/api/assets` | Manage registered assets |
| `/api/signals` | Retrieve AI bias signals |
| `/api/charts` | Return Plotly JSON / PNG charts |
| `/api/training` | Trigger historical retraining |

---

### Security & Governance

* Immutable Graylog logging  
* Role-based access (read / write separation)  
* Versioned datasets and model IDs  
* Audit trail for every signal and model run

---
