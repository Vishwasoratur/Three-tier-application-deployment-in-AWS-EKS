# Three-tier-architecture-application-deployment-in-AWS-EKS
This repository contains the deployment scripts and configurations for a Vote Counting Application following a three-tier architecture on AWS EKS (Elastic Kubernetes Service).

Frontend: The frontend of this application is built using React and JavaScript. It provides a responsive and user-friendly interface for casting votes.

Backend and API: The backend of this application is powered by Go (Golang). It serves as the API handling user voting requests. MongoDB is used as the database backend, configured with a replica set for data redundancy and high availability.

STEPS TO DEPLOY:

DATABASE:
kubectl apply -f mongo-statefulset.yaml
kubectl apply -f mongo-service.yaml
kubectl apply -f mongodb-secret.yaml

Pass the data to the mongodb.

BACKEND:
kubectl apply -f backend-deployment.yaml
kubectl apply -f backend-service.yaml

FRONTEND:
kubectl apply -f frontend-deployment.yaml
kubectl apply -f frontend-service.yaml


