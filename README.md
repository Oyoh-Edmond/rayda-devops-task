# Rayda DevOps Engineer Assessment

This is a production-grade deployment setup for a FastAPI microservice, prepared for containerization, Kubernetes orchestration, monitoring, and automation using CI/CD and Terraform.

---

## ✅ Features

* Dockerized FastAPI app
* Kubernetes manifests (`k8s/`)
* CI/CD support via GitHub Actions
* Infrastructure provisioning via Terraform
* Monitoring setup with Prometheus/Grafana
* Secure handling with secrets, RBAC, and best practices

---

## 🗂️ Project Structure

```
production-deployment/
├── .github/
│   └── workflows/              # GitHub Actions CI/CD pipelines
│       └── deploy.yml
├── app/                        # FastAPI source code
│   ├── main.py                 # Main application
│   └── requirements.txt        # Python dependencies
├── k8s/                        # Kubernetes YAML manifests
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   ├── configmap.yaml
│   ├── secret.yaml
│   ├── hpa.yaml
│   ├── serviceaccount.yaml
│   └── networkpolicy.yaml
├── monitoring/                 # Monitoring tools config (Prometheus, Grafana, etc.)
├── security/                   # RBAC, policies, TLS, secret management
├── scripts/                    # Automation scripts (deployment, backup, etc.)
├── terraform/                  # Infrastructure-as-Code (e.g., AWS, GCP resources)
├── Dockerfile                  # Production-grade Dockerfile
├── README.md                   # This file
└── RUNBOOK.md                  # Operational playbook for deployment, monitoring, recovery
```

---

## 📦 Requirements

* Docker
* Git
* (Optional) Minikube or Kind (for local Kubernetes testing)
* (Optional) Terraform CLI


---

## 🚀 How to Run Locally

```bash
docker build -t fastapi-prod .
docker run -p 8000:8000 fastapi-prod
```

Access the app at:

* Health check: [http://localhost:8000/health](http://localhost:8000/health)
* Items list: [http://localhost:8000/items](http://localhost:8000/items)

img


## 🧑‍💻 Author

Edmond Oyoh
