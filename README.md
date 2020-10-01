# EKS Cluster (no frills) 
# CloudFormation + AWS CLI (kubectl/ecsctl commands)

Hello World Outline/Process

- Create an AWS IAM service role and an AWS VPC.
- Launch an EC2 Instance and Configure the Command Line Tools
(EKSCtl / KubeCtl)
- Create Amazon EKS cluster.
(EKSctl) -> created worker nodes

```sh
ksctl create cluster --name dev --version 1.16 --region us-east-1 --nodegroup-name standard-workers --node-type t3.micro --nodes 3 --nodes-min 1 --nodes-max 4 --managed
```
- Configure kubectl for Amazon EKS cluster.
- Launch and configure Amazon EKS worker nodes.
- Launch a simple nginx application.
 - Created LB service and connected backend app (NGINX) to the LB (Pods/ReplicaSets/Nodes)
 
-create the service
```sh 
kubectl apply -f ./nginx-svc.yaml
```
-create the deployment
```sh 
kubectl apply -f ./nginx-deployment.yaml
```
- Cleaning up the application & assigned resources.
 
 
# EKS NGINX Hello World (CF & Nginx Yamls)
 -  nginx-deployment.yaml
 -  nginx-svc.yaml

