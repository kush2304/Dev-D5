# Dev-D5
 Build a Kubernetes Cluster Locally with Minikube
* Tools Used
 Minikube
 kubectl
 Docker
 AWS EC2 (Ubuntu)

* Files
deployment.yaml – NGINX Deployment (2 replicas)
service.yaml – NodePort Service to expose NGINX
screenshots/ – Folder for command output and browser screenshots

* Steps
Start Minikube:
minikube start --driver=docker

Apply YAMLs:
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

Port Forward and Test:
kubectl port-forward svc/nginx-service 8080:80
Visit http://<your-ec2-ip>:8080
