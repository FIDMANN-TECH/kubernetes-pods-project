# 🧩 Working with Kubernetes Pods

(With Advanced Extension: Deployments & ReplicaSets)

## 📌 Project Overview

This project demonstrates practical, hands-on experience working with Kubernetes Pods, the smallest and most fundamental unit of deployment in Kubernetes.

The project begins with standalone Pods to build foundational understanding and is later extended with Deployments and ReplicaSets to demonstrate how real-world, production-grade Kubernetes workloads are managed.

This progression mirrors how Kubernetes is learned and used in professional DevOps environments.

## 🎯 Project Objectives

By completing this project, the following Kubernetes concepts are demonstrated:

Creating and managing Pods

Inspecting Pod configuration and lifecycle

Viewing application logs

Using labels and selectors

Understanding Pod ephemerality

Cleaning up Kubernetes resources

(Advanced) Managing workloads with Deployments & ReplicaSets

(Advanced) Self-healing, scaling, and rolling updates

## 🛠️ Tools & Technologies Used

Kubernetes

Minikube

kubectl

Docker

Linux (Ubuntu)

### 📁 Project Structure
kubernetes-pods-project/
├── pods/
│   └── nginx-pod.yaml
│
├── deployments/                 # Advanced extension
│   └── nginx-deployment.yaml
│
├── README.md
│
└── screenshots/
    ├── pods/
    │   ├── 01_tools_installed_versions.png
    │   ├── 02_cluster_running.png
    │   ├── 03_nodes_ready.png
    │   ├── 04_nginx_pod_running.png
    │   ├── 05_pod_description.png
    │   ├── 06_pod_logs.png
    │   ├── 07_nginx_browser_access.png
    │   ├── 08_yaml_pod_created.png
    │   ├── 09_pod_labels.png
    │   ├── 10_pod_deleted.png
    │   └── 11_cleanup_complete.png
    │
    └── deployments/
        ├── 01_nodes_ready_deployment.png
        ├── 02_deployment_pods_running.png
        ├── 03_replicaset_details.png
        ├── 04_self_healing_pod_recreated.png
        ├── 05_deployment_scaled.png
        ├── 06_rolling_update_success.png
        ├── 07_rollback_success.png
        ├── 08_service_exposed.png
        └── 09_cleanup_deployment.png

## 🚀 Part 1: Working with Kubernetes Pods (Core Project)
### 1️⃣ Cluster Setup & Verification

The Kubernetes cluster was initialized using Minikube and verified using kubectl.

Evidence:

Tool installation verification

Cluster status confirmation

Node readiness check


### 2️⃣ Creating a Pod (Imperative Method)

A basic Nginx Pod was created using the imperative approach to understand direct Pod creation.

Key concepts demonstrated:

Pod creation

Container image usage

Pod lifecycle


### 3️⃣ Pod Inspection & Debugging

The Pod was inspected using:

kubectl describe pod

kubectl logs

This provided visibility into:

Scheduling events

Container configuration

Application logs


### 4️⃣ Accessing the Pod

The application running inside the Pod was accessed locally using port forwarding, confirming successful deployment.


### 5️⃣ Creating a Pod Using YAML (Declarative Method)

A declarative YAML file was used to define and create a Pod, reinforcing infrastructure-as-code principles.


### 6️⃣ Labels & Selectors

Labels were applied and queried to demonstrate how Kubernetes groups and filters resources.


### 7️⃣ Pod Deletion & Cleanup

The Pod was manually deleted to demonstrate its ephemeral nature.

Key takeaway:

Standalone Pods do not self-heal.

---

## 🚀 Part 2: Advanced Extension — Deployments & ReplicaSets

#### ⚠️ This section is an advanced extension added to demonstrate production-grade Kubernetes usage.
The core focus of the project remains Kubernetes Pods.

### 🔁 Why Deployments?

In real-world Kubernetes environments:

Pods are not created directly

Controllers manage Pods for reliability and scalability

Deployments provide:

Self-healing

Scaling

Rolling updates

Rollbacks

### 1️⃣ Creating a Deployment

A Deployment was created with multiple replicas of the Nginx container.


### 2️⃣ Understanding ReplicaSets

The Deployment automatically created a ReplicaSet responsible for maintaining the desired number of Pods.



### 3️⃣ Self-Healing Demonstration

A Pod managed by the Deployment was manually deleted. Kubernetes immediately recreated it.


### 4️⃣ Scaling the Application

The Deployment was scaled from 3 to 5 replicas using kubectl scale.


### 5️⃣ Rolling Updates & Rollback

A rolling update was performed by changing the container image version, followed by a rollback to the previous version.


### 6️⃣ Exposing the Deployment (Optional Bonus)

The Deployment was exposed using a Kubernetes Service and accessed via Minikube.

### 7️⃣ Cleanup

All Deployment-related resources were deleted, and the cluster was stopped.


## 🧠 Key Learnings

Pods are ephemeral and not production-ready by themselves

Deployments manage ReplicaSets, which manage Pods

Kubernetes provides built-in self-healing

Scaling and rolling updates are first-class Kubernetes features

Declarative configuration is preferred in real-world DevOps workflows

## 🏆 DevOps Skills Demonstrated

Kubernetes fundamentals

Linux command-line proficiency

YAML-based configuration management

Debugging and troubleshooting

Production-aligned documentation

Clean project structuring

## Below are screenshots of workflow:
![tools-installed](./img/01_tools_installed_versions.png)
![cluster-running](./img/02_cluster_running.png)
![node-ready](./img/03_nodes_ready.png)
![nginx-pod-running](./img/04_nginx_pod_running.png)
![pod-description](./img/05_pod_description.png)
![pod-logs](./img/06_pod_logs.png)
![nginx-browser](./img/07_nginx_browser_access.png)
![yaml-pod-created](./img/08_yaml_pod_created.png)
![pod-labels](./img/09_pod_labels.png)
![pod-deleted](./img/10_pod_deleted.png)
![cleanup](./img/11_cleanup_complete.png)
![nodes-ready-deployment](./img/12_nodes_ready_deployment.png)
![deployment-pod-running](./img/13_deployment_pods_running.png)
![replicaset-details](./img/14_replicaset_details.png)
![self-healing-pod-recreated](./img/15_self_healing_pod_recreated.png)
![deployment-scaled](./img/16_deployment_scaled.png)
![rolling-uphdate-success](./img/17_rolling_update_success.png)
![rollback-success](./img/18_rollback_success.png)
![service-expose](./img/19_service_exposed.png)
![cleanup-deployment](./img/20_cleanup_deployment.png)