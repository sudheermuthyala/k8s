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
- EKS Automatically detects and replaces unhealthy control plane instances, restart then across the Availability Zones With in the region as needed.
## Worker Nodes & Node Groups
- Group of EC2-Instances Where we run our Application WorkLoads 
- worker machines in kubernets are called nodes This are Nothing but EC2 instances
- EKS worker nodes run in AWS account And connect to our cluster's control plane via the cluster API Server endpoint.
- A node group is one or more EC2-instances That are deployed in an EC2 Autoscalling group
- All instances in the node group must
  1. Be the Same instance type
  2. Be running the same AMI
  3. use same EKS worker Node IAM role

## Fargate Profiles(Serverless)
- Instade of EC2-Instances We run our Application Worklode on Serverless Fargate Profiles
- AWS fargate is a technology that provides On-demand, right-sized computer capacity for containers
- With fargate , we no longer Have to provisen , configure or scale groups of virtual machines to run containers.
- Each pod running on fargate has its own isolated boundary and does not share the underlying kernel CPU resources, Memoryre sources or elastic Network interface with another pod
- AWS specially built fargate controllers that recognizes the pods belonging to fargate and schedules them on fargate profiles.
## VPC 
- With AWS VPC we follow secure Networking Standards Which will allow us to run Production workloads on EKS
- EKS uses the AWS VPC Network profiles to restrict traffic between control plane components to with in asingle cluster 
- controle plane components for a EKS cluster Cannot view or receive communications from other cluster or other AWS account, except an Authorized with Kubernets RBAC policies.
- This secure highly avallable configuration makes EKS Reliable and Recomended for Production Workloads  


