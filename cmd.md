#### Prashant Docker Repository -
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

docker hub:
client - done
api-gateway - done
entries-service - done
files-service - done
moods-api - done
moods-service - done
server-main - done
stats-api - done
stats-service - done

**KUBECTL Commands**

`kubectl get ns` -> to get name space <br>
`kubectl get pods` -> to get list of pods <br>
`Kubectl config get-contexts`-> to get the list of kubernetes clusters <br>
`kubectl config current-context` -> to get the current cluster <br>
`kubectl config use-context docker-desktop` <br>

`kubectl apply -f k8s/env/config-secrets.yml` to create a pod <br>