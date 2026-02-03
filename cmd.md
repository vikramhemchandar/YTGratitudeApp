## List of Docker and Kubernetes commands used for this project

##### Prashant Docker Repository -
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
- client
##### Backend
- api-gateway
- entries-service
- files-service 
- moods-api 
- moods-service
- server-ma
- stats-api
- stats-service

#### KUBECTL Commands

##### List Objects
To get the list of kubernetes clusters 
>kubectl config get-contexts<br>
To get the current cluster
>kubectl config current-context
<br> 
`kubectl config use-context docker-desktop` <br>
`kubectl get ns` : to get name space <br>
`kubectl get pods` : to get list of pods <br>
`kubectl get deployments` : to get list of deployments <br>
`kubectl get services` : to get list of services <br>
`kubectl get secrets` : to get list of secret <br>
`kubectl get configmaps` : to get list of configmap <br>
`kubectl get pv` : to get list of database persistant volume <br>
`kubectl get pvc` : to get list of database persistant volume claim <br>

##### Create Objects
`kubectl apply -f k8s/env/config-secrets.yml` to create a Secret object<br>
`kubectl apply -f k8s/env/configmap.yml` to create a ConfigMap object <br>
`kubectl apply -f k8s/database/database-pv.yml` to create Database Persistant Volume <br>
`kubectl apply -f k8s/database/database-persistant-vlc.yml` to create Database Persistant Volume claim <br>
`kubectl apply -f k8s/database/database-deployment.yml` to create Deployment object for Database<br>
`kubectl apply -f k8s/database/database-service.yml` to create Service object for Database<br>
`kubectl apply -f k8s/frontend/client-deployment.yml` to create deployment object for Client service<br>
`kubectl apply -f k8s/frontend/client-service.yml` to create service object for Client service<br>
`kubectl apply -f k8s/backend/api-gateway-deployment.yml` to create deployment object for api-gateway service<br>
`kubectl apply -f k8s/backend/api-gateway-service.yml` to create service object for api-gateway service<br>
