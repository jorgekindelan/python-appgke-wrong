# python-appgke-wrong

> **Educational repository for practicing Google Kubernetes Engine (GKE) deployment with GitHub Actions, including intentional mistakes for troubleshooting exercises.**

---

## 👤 Author

- **Name:** Juan Vicente Herrera Ruiz de Alejo
- **GitHub:** [@juanviz](https://github.com/juanviz)
- **Affiliation:** ICAI

---

## 🧩 Project purpose

This repository contains a simple Flask application and resources meant to help practice:

- Deploying an app to **GKE** using `kubectl` and YAML manifests.
- Building and pushing Docker images to **Google Container Registry (GCR)**.
- Automating deployments with **GitHub Actions**.
- Troubleshooting CI/CD pipelines and deployment issues.

> ⚠️ Some common errors have been intentionally left in the configuration to encourage practical troubleshooting.

---

## 📁 Repository structure

- `currency_converter.py` – Flask app (simple web server).
- `requirements.txt` – Python dependencies.
- `Dockerfile` – Docker image for the app.
- `k8s/deployment.yaml` – Kubernetes Deployment manifest.
- `k8s/service.yaml` – Kubernetes Service manifest.
- `.github/workflows/deploy.yml` – GitHub Actions workflow to build and deploy to GKE.
- `templates/index.html` – HTML UI for currency conversion.


#
## ⚙️ GitHub Actions: deploy to GKE

The main workflow is located at `.github/workflows/deploy.yml` and is triggered on `push` to the `main` branch.

### Required secrets (Repository Settings > Secrets)

- `GCP_PROJECT_ID` – GCP project ID.
- `GKE_CLUSTER` – GKE cluster name.
- `GKE_ZONE` – Cluster zone (e.g. `us-central1-a`).
- `GCP_SA_KEY` – JSON key for a service account with deploy and storage permissions.


