# End-to-End DevSecOps & GitOps Pipeline

### ⚠️ Project Scope
* **Application Code:** Forked from `Ashfaque-9x/register-app` to serve as a functional base application.
* **My Contribution:** I engineered the cloud infrastructure, CI/CD pipeline, and Kubernetes deployment architecture for this application from scratch.

### 🚀 My DevOps Contributions
I utilized this repository to focus 100% on DevOps infrastructure and automation. My original work includes:
* **CI/CD Pipeline Automation:** Wrote the `Jenkinsfile` to fully automate the build, test, and deployment lifecycle.
* **Kubernetes Orchestration:** Authored and configured the `deployment.yaml` and `service.yaml` manifests for deployment to an Amazon EKS cluster.
* **GitOps Delivery:** Configured **Argo CD** to monitor this repository and automatically sync state changes to the Kubernetes cluster with zero downtime.
* **DevSecOps Integration:** Implemented strict quality gates using SonarQube (SAST) and Trivy to block container vulnerabilities before pushing to the registry.

### 🔄 Pipeline Architecture
1. Developer pushes code to GitHub.
2. Webhook triggers Jenkins build on AWS EC2.
3. Jenkins runs SonarQube analysis and Trivy image scans.
4. Docker image is built and pushed to the container registry.
5. Kubernetes manifests (`deployment.yaml`) are updated.
6. Argo CD detects the drift and automatically deploys the updated state to EKS.

### 🛠️ Tech Stack
* **Cloud & Orchestration:** AWS (EC2, EKS), Kubernetes, Docker
* **CI/CD & GitOps:** Jenkins, Argo CD, GitHub
* **Security:** SonarQube, Trivy
