Amazon EKS Hands-On Learning Journey
Overview
This repository contains the YAML manifests, configurations, and practical exercises used
during a complete hands-on Amazon EKS (Elastic Kubernetes Service) learning journey.
The goal of this project was not just to learn Kubernetes concepts theoretically, but to
deploy, operate, troubleshoot, monitor, and eventually clean up a real EKS environment on
AWS.
By the end of this journey, the cluster was built from scratch, applications were deployed,
storage was configured, workloads were scaled, monitoring was enabled, and the entire
infrastructure was safely decommissioned.
Learning Objectives
After completing all phases, you should understand:
• Kubernetes Architecture
• Amazon EKS Fundamentals
• Pods and Deployments
• Services and Networking
• ConfigMaps and Secrets
• Persistent Storage
• AWS EBS Integration
• Ingress and External Access
• Horizontal Pod Autoscaling (HPA)
• Namespaces and Resource Governance
• Stateful Applications
• Monitoring with Prometheus and Grafana
• Infrastructure Cleanup and Cost Optimization

Phase 1 - EKS Foundation
Topics Covered:
• Amazon EKS Architecture
• Control Plane vs Worker Nodes
• kubectl Configuration
• Cluster Verification
Outcome: Successfully created and connected to an EKS cluster.

Phase 2 - Pods
Topics Covered:
• Pod Lifecycle
• Pod Scheduling
• Logs
• Pod Deletion
• Self-Healing Concepts
Outcome: Deployed and managed standalone pods.

Phase 3 - Deployments
Topics Covered:
• Deployments
• ReplicaSets
• Scaling
• Rolling Updates
• Self-Healing
Outcome: Managed applications using Deployments and multiple replicas.

Phase 4 - Services
Topics Covered:
• ClusterIP
• NodePort
• LoadBalancer
Outcome: Exposed applications internally and externally.

Phase 5 - ConfigMaps and Secrets
Topics Covered:
• Externalized Configuration
• Secret Management
• Environment Variables
• Volume Mounts
Outcome: Separated application configuration from container images.

Phase 6 - Persistent Storage
Topics Covered:
• Persistent Volumes (PV)
• Persistent Volume Claims (PVC)
• Storage Classes
Outcome:
Introduced persistent storage concepts in Kubernetes.

Phase 7 - AWS EBS Integration
Topics Covered:
• EBS CSI Driver
• Dynamic Volume Provisioning
• Persistent Data
Lab:
• Write data to a volume
• Delete pod
• Verify data survives
Outcome: Learned how Kubernetes integrates with AWS EBS storage.

Phase 8 - Ingress
Topics Covered:
• Ingress
• Ingress Controllers
• Path-Based Routing
• External Traffic Management
Outcome: Exposed applications through centralized routing.

Phase 9 - Horizontal Pod Autoscaling
Topics Covered:
• Metrics Server
• CPU Requests
• CPU Limits
• Horizontal Pod Autoscaler (HPA)
Lab:
• Generate CPU load
• Observe automatic scaling
Outcome: Implemented automatic workload scaling.

Phase 10 - Namespaces and Governance
Topics Covered:
• Namespaces
• ResourceQuota
• LimitRange
Outcome: Learned workload isolation and resource governance.

Phase 11 - Stateful Applications
Topics Covered:
• StatefulSets
• Headless Services
• Stable Pod Identity
• Persistent Storage per Pod
Lab:
• Stateful NGINX Deployment
• DNS-Based Pod Discovery
• Persistent EBS Volumes
Outcome:
Learned how stateful workloads differ from stateless workloads.

Phase 12 - Monitoring and Observability
Topics Covered:
• Helm
• Prometheus
• Grafana
• AlertManager
• Node Exporter
• Kube State Metrics
Lab:
• Deploy kube-prometheus-stack
• Visualize CPU and Memory Metrics
• Generate Load
• Observe Cluster Metrics
Outcome: Implemented a complete monitoring stack for EKS.

Phase 13 - Cleanup and Cost Optimization
Topics Covered:
• Resource Inventory
• Load Balancer Cleanup
• PVC Cleanup
• Monitoring Stack Removal
• Cluster Decommissioning
Outcome: Safely removed all AWS resources and minimized cloud costs.

Key Troubleshooting Scenarios Encountered
This repository also documents real issues encountered during hands-on practice:
• PVC Pending due to missing StorageClass
• StatefulSet immutable field errors
• Headless Service DNS troubleshooting
• HPA showing Unknown metrics
• Missing CPU Requests
• Label collisions between Deployments and StatefulSets
• Grafana access issues
• PVC stuck in Terminating state
• EKS cleanup and resource deletion verification
These troubleshooting exercises provided some of the most valuable learning throughout
the journey.

Repository Structure
Typical files included:
deployment.yaml
service.yaml
configmap.yaml
secret.yaml
pv.yaml
pvc.yaml
ingress.yaml
hpa.yaml
headless-service.yaml
statefulset-storage.yaml

Important Notes
Never commit:
• AWS Credentials
• PEM Key Files
• kubeconfig Files
• Secrets containing real passwords
Always use:
• Kubernetes Secrets
• Environment Variables
• Secure Secret Management Practices

Final Outcome
This project demonstrates a complete Kubernetes lifecycle on Amazon EKS:
Cluster Creation
→ Application Deployment
→ Configuration Management
→ Persistent Storage
→ Networking
→ Autoscaling
→ Monitoring
→ Troubleshooting
→ Cleanup
The objective was not only to learn Kubernetes concepts but also to gain practical
operational experience similar to real-world cloud environments.
