# 🚀 Super Mario Deployment on AWS EKS

This project demonstrates provisioning infrastructure using Terraform and deploying a containerized Super Mario application on Amazon EKS. The application is exposed publicly via an AWS LoadBalancer.

---

## 📌 Tech Stack

- AWS
- Amazon EKS
- Terraform
- Kubernetes
- EC2 Node Group
- S3 Remote Backend
- AWS LoadBalancer

---

## 🏗 Architecture Flow

User  
↓  
AWS LoadBalancer  
↓  
EKS Node Group (EC2)  
↓  
Kubernetes Pods (Mario Container)

---

## ⚙️ Complete Execution Flow

Run everything in this exact order:

Provision Infrastructure:

cd EKS-TF  
terraform init  
terraform apply  

Configure Kubernetes:

aws eks update-kubeconfig --name EKS_CLOUD --region us-east-1  

Deploy Application:

kubectl apply -f deployment.yaml  
kubectl apply -f service.yaml  

Verify:

kubectl get pods  
kubectl get svc  

---

## 🌐 Access Application

Once LoadBalancer is created, open:

http://<AWS-LoadBalancer-DNS>

---
---

## 📸 Deployment Screenshots

### 🎮 Super Mario Application Running
![Mario Output](screenshots/mario.png)

---

### ☸️ Amazon EKS Cluster
![EKS Cluster](screenshots/eks.png)

---

### 🖥 EC2 Instance
![EC2 Instance](screenshots/ec2.png)

---

### 🪣 S3 Backend (Terraform State)
![S3 Bucket](screenshots/s3.png)



## 👨‍💻 Author

Bhushan Malpure  
DevOps Engineer  
AWS | Terraform | Kubernetes
