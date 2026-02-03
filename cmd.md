## List of Docker and Kubernetes commands used for this project

##### Docker Images in Docker Hub
```
Frontend:
prashantdey/completeprojectb14:clientv1.0
Backend:
prashantdey/completeprojectb14:apigatewayv1.0
prashantdey/completeprojectb14:entriesservicev1.0
prashantdey/completeprojectb14:filesservicev1.0
prashantdey/completeprojectb14:moodsapiv1.0
prashantdey/completeprojectb14:moodsservicev1.0
prashantdey/completeprojectb14:servermainv1.0
prashantdey/completeprojectb14:statsapiv1.0
prashantdey/completeprojectb14:statsservicev1.0
```

To build client docker file – 
>docker build -f ./client/Dockerfile -t vikramhemchandar/ytgratitudeapp:clientv1.0 .

To build client api-gateway file – 
>docker build -f ./services/api-gateway\Dockerfile -t vikramhemchandar/ytgratitudeapp:api-gatewayv1.0 .

To push to docker hub – 
>docker push vikramhemchandar/ytgratitudeapp:clientv1.0

#### Microservices details 
##### Frontend:
- client <br>
##### Backend
- api-gateway
- entries-service
- files-service 
- moods-api 
- moods-service
- server-ma
- stats-api
- stats-service

#### Kubernetes Commands

##### AWS Kubernetes Cluster
`eksctl create cluster --name vikramhemchandar-eks-cluster --region ap-south-1 --nodegroup-name standard-workers --node-type t3.medium --nodes 3 --nodes-min 2 --nodes-max 4` to create a cluster on AWS for ap-south-1 Region, with 3 nodes<br>
`aws eks --region ap-south-1 update-kubeconfig --name vikramhemchandar-eks-cluster` to add a new context <br>
`kubectl config get-contexts` to get the list of Kubernetes clusters <br>
`kubectl config current-context` to get the current Kubernetes cluster <br>

##### Create Objects
`kubectl apply -f k8s/env/config-secrets.yml` to create a Secret object<br>
`kubectl apply -f k8s/env/configmap.yml` to create a ConfigMap object <br>
`kubectl apply -f k8s/database/database-pv.yml` to create Database Persistant Volume <br>
`kubectl apply -f k8s/database/database-persistant-vlc.yml` to create Database Persistant Volume claim <br>
`kubectl apply -f k8s/database/database-deployment.yml` to create Deployment object for Database<br>
`kubectl apply -f k8s/database/database-service.yml` to create Service object for Database<br>
`kubectl apply -f k8s/frontend/client-deployment.yml` to create Deployment object for Client microservice<br>
`kubectl apply -f k8s/frontend/client-service.yml` to create Service object for Client microservice<br>
`kubectl apply -f k8s/backend/api-gateway-deployment.yml` to create Deployment object for api-gateway microservice<br>
`kubectl apply -f k8s/backend/api-gateway-service.yml` to create Service object for api-gateway microservice<br>
`kubectl apply -f k8s/backend/entries-service-deployment.yml` to create Deployment object for entries-service microservice<br>
`kubectl apply -f k8s/backend/entries-service-service.yml` to create Service object for entries-service microserviceservice<br>
`kubectl apply -f k8s/backend/files-service-deployment.yml` to create Deployment object for files-service microservice<br>
`kubectl apply -f k8s/backend/files-service-service.yml` to create Service object for files-service microserviceservice<br>
`kubectl apply -f k8s/backend/moods-api-deployment.yml` to create Deployment object for moods-api microservice<br>
`kubectl apply -f k8s/backend/moods-api-service.yml` to create Service object for moods-api microserviceservice<br>
`kubectl apply -f k8s/backend/moods-service-deployment.yml` to create Deployment object for moods-service microservice<br>
`kubectl apply -f k8s/backend/moods-serivce-service.yml` to create Service object for moods-service microserviceservice<br>
`kubectl apply -f k8s/backend/server-main-deployment.yml` to create Deployment object for server-main microservice<br>
`kubectl apply -f k8s/backend/server-main-service.yml` to create Service object for server-main microserviceservice<br>
`kubectl apply -f k8s/backend/stats-api-deployment.yml` to create Deployment object for stats-api microservice<br>
`kubectl apply -f k8s/backend/stats-api-service.yml` to create Service object for stats-api microserviceservice<br>
`kubectl apply -f k8s/backend/stats-service-deployment.yml` to create Deployment object for stats-service microservice<br>
`kubectl apply -f k8s/backend/stats-service-service.yml` to create Service object for stats-service microserviceservice<br>

##### List Objects
`kubectl config get-contexts` to get the list of kubernetes clusters <br> 
`kubectl config current-context` to get the current cluster <br>
`kubectl config use-context docker-desktop` to use another cluster <br>
`kubectl get ns` : to get name space <br>
`kubectl get pods` : to get list of pods <br>
`kubectl get deployments` : to get list of deployments <br>
`kubectl get services` : to get list of services <br>
`kubectl get secrets` : to get list of secret <br>
`kubectl get configmaps` : to get list of configmap <br>
`kubectl get pv` : to get list of database persistant volume <br>
`kubectl get pvc` : to get list of database persistant volume claim <br>

#### Delete Objects
`kubectl delete pod <pod-name>` to delete pod <br>
`kubectl delete deployment <deployment-object-name>` to delete Ddeployment object <br>
`kubectl delete service <service-object-name>` to delete Service object <br>
`kubectl delete pvc <pvc-object-name>` to delete Database Persistant Volume object <br>
`kubectl delete pv <pv-object-name>` to delete Database Persistant Volume Claim object <br>
`kubectl delete configmap <configmap-object-name>` to delete ConfigMap object <br>
`kubectl delete secrets <configmap-object-name>` to delete Secrets object <br>

#### Create object files on Terminals
`kubectl create deployment nginx --image=nginx --dry-run=client -o yaml` to create a Deployment file <br>
`kubectl create service nginx --image=nginx --dry-run=client -o yaml` to create a Service file <br>
