# Web description: Kubernetes Section - Project Phase II

### web application as a Kubernetes Pod.
kubectl run webapp --image=galitoshri/webapp:1.1 --port=5000


### Deployment and ReplicaSet for managing the application.

### create deployment
kubectl create deployment webapp --image=galitoshri/webapp:1.1

### add replicas
kubectl scale deployment/webapp --replicas=3

### expose to port 5000
kubectl expose deployment webapp --type=NodePort --port=5000

### applying development,  service, hpa, and configmap with file
kubectl apply -f webapp_deployment.yaml  
kubectl apply -f webapp_service.yaml  
kubectl apply -f webapp_configmap.yaml  
kubectl apply -f webapp_hpa.yaml  
kubectl apply -f webapp_cronjob.yaml  



