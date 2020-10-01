# EKS Cluster (no frills) 
# CloudFormation + AWS CLI (kubectl/ecsctl commands)



EKS NGINX Hello World Outline
> in a nutshell; create an EC2, download the key software (Git,EKSctl,KubeCtl)
> use EKSctl to spawn the cluster (Its that simple)
> use Kubectle to configure the cluster and 'control' the cluster
> simple deployments can be done with kubectle and the CF templates for NGINX


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
 
 
# EKS NGINX Hello World (CF & NGINX Yamls)
 -  nginx-deployment.yaml
 -  nginx-svc.yaml

