## AWS EKS - Core Objects

# EKS - Cluster
- EKS Control Plane
- Worker Nodes & Node Groups
- Fargate Profiles(Serverless)
- VPC

## EKS Control Plane
- EKs Control Plain Contains Kubernets Master Components like **`etcd , KubeapiServer, KubeControler `** it's managed  Service By AWS
- EKS runs a Single tenant Kubernets control plane for each cluster,and control plane infrastructure is not shared acreoss the clusters or AWS Accounts
- This conteol plane consists of at least **two API Server Nodes, And three etcd Nodes** That runs Across the three availability zones within the Region
- EKS Automatically detects and replaces unhealthy control plane instances, restart then across the Availability Zones With in the region  as needed.
## Worker Nodes & Node Groups
- Group of EC2-Instances Where we run our Application WorkLoads 

## Fargate Profiles(Serverless)
- Instade of EC2-Instances We run our Application Worklode on Serverless Fargate Profiles
## VPC 
- With AWS VPC we follow secure Networking Standards Which will allow us to run Production workloads on EKS


