# Cloud-Native Web Voting Application with Kubernetes

This cloud-native web application is built using a mix of technologies. It's designed to be accessible to users via the internet, allowing them to vote for their preferred programming language out of six choices: **C#, Python, JavaScript, Go, Java, and NodeJS**.

---

## 🛠 Technical Stack

- **Frontend:** React + JavaScript (responsive, user-friendly UI for voting)
- **Backend & API:** Go (Golang) + MongoDB (replica set for redundancy & HA)
- **Database:** MongoDB with replica set
- **Orchestration:** Kubernetes

---

## 📦 Kubernetes Resources Used

- **Namespace:** Isolated environments for different components  
- **Secret:** Secure storage of API keys/credentials  
- **Deployment:** Manages app instances, scaling, updates  
- **Service:** Routes traffic to appropriate pods  
- **StatefulSet:** For MongoDB replica set  
- **PersistentVolume & PersistentVolumeClaim:** Data persistence & scalability  

---

## 🎯 Learning Opportunities

By working on this project, you will gain hands-on experience with:

- **Containerization** (Docker)  
- **Kubernetes orchestration** for deployments & scaling  
- **Microservices architecture** (decoupled frontend & backend)  
- **MongoDB replica set setup**  
- **Secrets management** in Kubernetes  
- **Stateful applications in Kubernetes**  
- **Persistent storage management**  

---

## 🚀 Steps to Deploy

📺 **YouTube Reference Video:**  
[Video Tutorial](https://www.youtube.com/@cloudchamp?)  
👉 Subscribe for more tutorials!

---

### 1️⃣ Create EKS Cluster

- Create **EKS cluster** with NodeGroup (`2 × t2.medium`)  
- Create optional **EC2 instance (t2.micro)**  

#### IAM Role for EC2
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": [
      "eks:DescribeCluster",
      "eks:ListClusters",
      "eks:DescribeNodegroup",
      "eks:ListNodegroups",
      "eks:ListUpdates",
      "eks:AccessKubernetesApi"
    ],
    "Resource": "*"
  }]
}
