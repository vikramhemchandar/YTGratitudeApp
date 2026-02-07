Order of executing the yaml scripts
1. database-secret.yml
2. openai-api-secret.yml
3. postgres-init-config.yml
4. postgres-deployment.yml
5. postgre-cluster-ip-service.yml
6. storageclass-gp3-default.yml
7. database-persistent-volume-claim.yml
then backend deployment and service objects
the frontend deployment and service objects
last ingress-service.yml