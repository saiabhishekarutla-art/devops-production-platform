# DevOps Production Platform Architecture

```mermaid
flowchart TD

Developer --> GitHub

GitHub --> CI_CD["GitHub Actions CI/CD"]

CI_CD --> Docker["Docker Image Build"]

Docker --> Registry["Container Registry"]

Registry --> Kubernetes["Kubernetes Cluster"]

Kubernetes --> App["Application (Nginx)"]

Kubernetes --> Prometheus["Prometheus Monitoring"]

Prometheus --> Grafana["Grafana Dashboards"]

Terraform --> AWS["AWS Infrastructure"]

AWS --> Kubernetes
