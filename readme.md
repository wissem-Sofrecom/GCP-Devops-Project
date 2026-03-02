# This is a realtime GCP/DEVOPS project #

# 🚀 GCP DevOps CI/CD Pipeline

Production-style CI/CD pipeline built on Google Cloud Platform to automate container builds and Kubernetes deployments.

---

## 🎯 Objective

Design and implement a complete DevOps workflow that:

- Builds a Python Flask application
- Containerizes it using Docker
- Automates builds via Google Cloud Build
- Deploys automatically to Google Kubernetes Engine (GKE)
- Supports controlled scaling via Kubernetes manifests

---

## 🏗 Architecture

GitHub → Cloud Build Trigger → Docker Build → Artifact Registry → GKE Deployment

**Workflow Overview:**

1. Developer pushes code to `main`
2. Cloud Build trigger starts automatically
3. Docker image is built and tagged with commit SHA
4. Image is pushed to Google Artifact Registry
5. Kubernetes deployment runs updated container
6. Application becomes available inside the cluster

---

## 🛠 Tech Stack

- **Python (Flask)**
- **Docker**
- **Google Cloud Build**
- **Google Artifact Registry**
- **Google Kubernetes Engine (GKE)**
- **kubectl / gcloud CLI**

---

## 📦 Repository Structure


.
├── app.py
├── Dockerfile
├── requirements.txt
├── cloudbuild.yaml
├── gke.yaml
└── README.md


---

## ⚙️ CI/CD Implementation

### 🔹 Continuous Integration

- Cloud Build trigger on `main`
- Docker image built with commit-based tagging
- Image pushed to Artifact Registry
- Fully automated — no manual build steps

### 🔹 Continuous Deployment

- Kubernetes manifest (`gke.yaml`) defines:
  - Deployment
  - Replica count
  - Service exposure
- Deployment updated using new image version
- Application runs inside GKE cluster

---

## ☸️ Kubernetes Highlights

- Dedicated deployment resource
- Scalable replica configuration
- Service abstraction for internal/external access
- Manual or declarative scaling support

Example scaling:


kubectl scale deployment my-app --replicas=5


---

## 🔐 Security & Permissions

Cloud Build service account configured with:

- Artifact Registry Writer
- Container Developer
- Storage Admin

Ensures secure automated image push and deployment.

---

## 🧪 Local Development

Run locally:


pip install -r requirements.txt
python app.py


Run with Docker:


docker build -t my-app .
docker run -p 8080:8080 my-app


---

## 📈 DevOps Concepts Demonstrated

- Automated CI pipeline
- Immutable container builds
- Kubernetes-based deployment
- Git-driven promotion workflow
- Infrastructure automation mindset
- Deployment scalability
- Production-style image tagging strategy

---

## 🚀 Key Achievements

✔ Fully automated Docker build pipeline
✔ Zero-manual production deployment
✔ Commit-based traceable image versions
✔ Kubernetes-native scaling capability
✔ Cloud-native CI/CD architecture

---

## 🔮 Future Enhancements

- Horizontal Pod Autoscaler (HPA)
- Multi-environment deployment (dev/prod namespaces)
- Monitoring integration (Prometheus / Grafana)
- GitOps workflow with ArgoCD
- Blue/Green deployment strategy

---

## 👨‍💻 Author

**Wissem Ben Houria**
DevOps & Cloud Engineer
Specializing in Kubernetes, CI/CD, and Google Cloud
