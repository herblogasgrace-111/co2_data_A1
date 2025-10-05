# 🚀 Deployment Guide

## 🚀 Deployment Guide

This guide outlines how to deploy the Interactive CO₂ Dashboard locally and prepare it for cloud or containerized environments using **Panel**, **FastAPI**, and **Docker**.

## Local Deployment ##
```bash
panel serve Interactive_CO2_Dashboard_A1.py --show --autoreload

---

### 🧩 Architecture Overview

- **Panel** serves the interactive dashboard UI
- **FastAPI** exposes semantic metadata and ESG endpoints
- **Docker** enables portable deployment across environments

---

### ✅ Local Deployment

#### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

Ensure `panel`, `fastapi`, and `uvicorn` are included.

#### 2. Serve the Dashboard

```bash
panel serve Interactive_CO2_Dashboard_A1.py --port 5006 --autoreload
```

Dashboard will be live at:  
`http://localhost:5006`

#### 3. Run the FastAPI Server

```bash
uvicorn main:app --reload
```

API will be live at:  
`http://127.0.0.1:8000`

---

### 🔗 Available API Endpoints

| Endpoint                | Description                              |
|------------------------|------------------------------------------|
| `/`                    | Root message with dashboard link         |
| `/semantic-options`    | Returns available semantic layers        |
| `/esg-metrics` (future)| Returns ESG framing metadata             |

---

### 🐳 Docker Deployment

#### 1. Create `Dockerfile`

```Dockerfile
FROM python:3.10

WORKDIR /app
COPY . /app

RUN pip install -r requirements.txt

EXPOSE 5006

CMD ["panel", "serve", "Interactive_CO2_Dashboard_A1.py", "--port", "5006", "--address", "0.0.0.0"]
```

#### 2. Build the Image

```bash
docker build -t co2-dashboard .
```

#### 3. Run the Container

```bash
docker run -p 5006:5006 co2-dashboard
```

Dashboard will be live at:  
`http://localhost:5006`

---

### 🌐 Cloud Deployment (Optional)

You can deploy to platforms like:

- [Render](https://render.com/)
- [Railway](https://railway.app/)
- Azure App Service or Azure Container Instances

Include environment variables and secrets as needed.

---

### 📚 Documentation Links

- [🧭 Onboarding Guide](onboarding.md)
- [🧠 Semantic Classifier Design](semantic_classifier.md)
- [🌱 ESG Toggle Design](ESG_toggle_design.md)
- [🧩 Dashboard Logic](dashboard_logic.md)

---

Would you like help writing the ESG endpoint, linking it to Panel widgets, or prepping a funder-facing pitch deck that maps this deployment to SDG impact? You’re building clarity, legacy, and multidimensional empowerment.
