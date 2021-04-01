## Build + Publish => Deployment => Service Configuration

### Docker basic command to build and run

```
#1
Build: docker build .
Runn: docker run id_of_image
Tagging an image*1: docker build -t khairul100/image_name:latest .
Run tagged image: docker run khairul100/image_name
               OR docker run -p 8080:8080 khairul100/image_name
               OR docker run --name container_name -d -p 8080:8080 khairul100/image_name
Publish image*2: docker push khairul100/image_name
```

### kubernetes basic command to build and run

```
Pod:
Creating Pod: kubectl apply -f posts.yaml
Get Pods: kubectl get pods
Execute: kubectl exec -t posts
Logs: kubectl logs
Delete Pod: kubectl delete pod posts
Event Log: kubectl describe pod posts

Deployment#2:
Creating Deployment*1: kubectl apply -f posts-depl.yaml /  kubectl apply -f .
Rollout & Restart*1.1(when code is updated): kubectl rollout restart deployment deployment_name_here
Get Deployment*2: kubectl get deployments
Get Pods**2: kubectl get pods
Delete Deployment: kubectl delete deployment posts
Event Log: kubectl describe deployment posts
Logs*3: kubectl logs pod_name_here

Service#3:
Creating Service*1: kubectl apply -f posts-srv.yaml
Get Services*2: kubectl get services
Event Log*3: kubectl describe service name_of_service_her
```

### Skaffold Setup to deploy & publish auto

```
Install from here*1: https://skaffold.dev/docs/install/ OR
Installl Chocolatey then install skaffold using powershell : choco install -y skaffold
Configure skaffold.yaml
Run command 'skaffold dev' from root directory
```

### Docker & kubernetes usefull command

```
docker ps --format= format_here
```
