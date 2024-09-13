# Infra-Setup-Details

### Practical Task for DevOps Engineer

#### Objective:
The goal of this task is to convert an existing setup of 100 Docker containers to Kubernetes, set up a Virtual Private Cloud (VPC), deploy on Azure Kubernetes Service (AKS), integrate pipelines with GitHub, implement reverse proxy and load balancing, ensure minimal downtime and fault tolerance, connect microservices using gRPC, use MongoDB as the backend database, secure the setup with Cloudflare, implement a zero-trust architecture, and set up Grafana for monitoring with defined thresholds.

#### Task Breakdown:

1. **Convert Docker to Kubernetes:**
   - Convert the existing 100 Docker containers to Kubernetes manifests (YAML files).
   - Ensure each service, volume, and network defined in Docker Compose is appropriately translated into Kubernetes deployments, services, ConfigMaps, Secrets, and Persistent Volume Claims.

2. **Set up Virtual Private Cloud (VPC):**
   - Configure a VPC in Azure to isolate the Kubernetes cluster and its resources.
   - Set up appropriate subnets, route tables, and network security groups to secure and manage traffic within the VPC.

3. **Set up Azure Kubernetes Service (AKS):**
   - Create a new AKS cluster within the configured VPC using the Azure portal or Azure CLI.
   - Configure the cluster with at least two nodes for high availability.
   - Ensure proper networking and security settings are applied.

4. **Integrate Pipelines with GitHub:**
   - Create a GitHub repository and push the Kubernetes manifests to it.
   - Set up CI/CD pipelines using GitHub Actions or Azure DevOps.
   - The pipeline should:
     - Lint and validate the Kubernetes manifests.
     - Build Docker images and push them to Azure Container Registry (ACR).
     - Deploy the application to AKS.

5. **Implement Reverse Proxy and Load Balancing:**
   - Set up NGINX or Traefik as an ingress controller to act as a reverse proxy.
   - Configure load balancing to distribute traffic evenly across the microservices.

6. **Ensure Minimal Downtime:**
   - Implement rolling updates in Kubernetes to ensure zero downtime during deployments.
   - Configure health checks and readiness probes for all services to ensure they are available before accepting traffic.

7. **Achieve Fault Tolerance:**
   - Configure Kubernetes to auto-restart failed containers and reschedule them on healthy nodes.
   - Set up horizontal pod autoscaling to handle varying loads.

8. **Connect Microservices using gRPC:**
   - Update the microservices to communicate with each other using gRPC.
   - Ensure proper service discovery and load balancing for gRPC services in Kubernetes.

9. **Backend Database with MongoDB:**
   - Deploy MongoDB as a stateful set in Kubernetes with persistent volume claims.
   - Configure MongoDB replicas for high availability and data redundancy.

10. **Secure with Cloudflare:**
    - Set up Cloudflare as a DNS provider and configure it to route traffic to the AKS cluster.
    - Enable Cloudflare's security features such as DDoS protection, WAF, and SSL/TLS encryption.

11. **Implement Zero-Trust Architecture:**
    - Configure network policies in Kubernetes to restrict communication between services to only what is necessary.
    - Implement Azure AD for authentication and role-based access control (RBAC) in AKS.
    - Use Azure Key Vault for managing and accessing secrets securely.
    - Enable logging and monitoring using tools like Azure Monitor and Prometheus to ensure continuous security compliance.

12. **Set up Grafana for Monitoring:**
    - Deploy Prometheus and Grafana in the AKS cluster.
    - Configure Prometheus to scrape metrics from Kubernetes and other services.
    - Set up Grafana dashboards to visualize metrics and performance data.
    - Define threshold alerts in Grafana for critical metrics such as CPU usage, memory usage, and response times.
    - Integrate alerts with email or other notification services to ensure timely response to incidents.

13. **Firewall and Security Monitoring:**
    - Configure Azure Firewall to manage and monitor traffic to and from the AKS cluster.
    - Set up security monitoring tools to detect and respond to potential threats.

#### Deliverables:
1. A GitHub repository containing:
   - Kubernetes manifests for all services.
   - CI/CD pipeline configuration files.
2. Documentation explaining:
   - Steps to set up the VPC and AKS cluster.
   - How to deploy the application using the CI/CD pipeline.
   - Configuration details for reverse proxy, load balancing, and fault tolerance.
   - gRPC communication setup between microservices.
   - MongoDB deployment and configuration.
   - Cloudflare setup and security configurations.
   - Zero-trust architecture implementation details.
   - Grafana and Prometheus setup, including dashboards and alert thresholds.
   - Firewall and security monitoring configurations.
3. A running instance of the application on AKS, accessible via a domain name managed by Cloudflare.

#### Evaluation Criteria:
- Correctness and completeness of the Kubernetes manifests.
- Successful deployment on AKS with minimal downtime and fault tolerance.
- Proper functioning of gRPC communication between microservices.
- Secure setup using Cloudflare and zero-trust architecture.
- Effective monitoring with Grafana and Prometheus, including defined thresholds and alerting.
- Comprehensive and clear documentation.
