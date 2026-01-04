AWS Prometheus + Grafana Monitoring Stack with CI/CD:

Project Overview
This project demonstrates a full DevOps workflow by deploying a Prometheus + Grafana monitoring stack on an AWS Free Tier EC2 instance using Docker containers. The entire deployment is automated with GitHub Actions, showcasing a real-world CI/CD pipeline that continuously updates the stack whenever changes are pushed to the repository.

Key Features:
Automated CI/CD Deployment: Every push to the main branch triggers GitHub Actions to SSH into EC2, pull the latest code, install Docker and Docker Compose if needed, and deploy the monitoring stack.
Containerized Services: Prometheus, Grafana, and Node Exporter run as isolated Docker containers, orchestrated with Docker Compose for seamless networking and management.
Preconfigured Dashboards: Grafana dashboards and Prometheus datasource are automatically provisioned, giving immediate visualization of CPU, Memory, Network, and Disk metrics.
Cloud Ready: Utilizes AWS EC2 Free Tier for hosting, with proper security group configuration for SSH, HTTP, and service ports.
Monitoring & Observability: Prometheus collects metrics from Node Exporter and itself, while Grafana provides real-time visualization and insights.

Workflow Overview:
AWS EC2 Setup: Ubuntu instance launched with Security Groups configured for SSH and service ports.
Dockerized Stack: Prometheus, Grafana, and Node Exporter are containerized and managed via Docker Compose.
CI/CD Pipeline: GitHub Actions workflow:
Connects to EC2 via SSH
Pulls the latest repository changes
Installs/updates Docker & Docker Compose
Runs docker-compose up -d to deploy or update containers
Dashboard Provisioning: Grafana dashboards and Prometheus datasources are loaded automatically from configuration files, eliminating manual setup.
Validation: Containers verified with docker ps; Prometheus targets confirmed as UP; dashboards display real-time metrics.

Skills Demonstrated:
DevOps Practices: CI/CD pipelines, automation, container orchestration
Cloud Infrastructure: AWS EC2 provisioning and security group management
Containerization: Docker, Docker Compose, multi-container networking
Monitoring & Observability: Prometheus metric collection, Grafana dashboard visualization
Automation: End-to-end automated deployment via GitHub Actions

Outcome:
After deployment:
Prometheus collects live metrics from the Node Exporter and itself.
Grafana dashboards visualize system metrics automatically.
Every code push triggers a fully automated redeployment, demonstrating a complete DevOps workflow from code to live monitoring.
