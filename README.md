### Start Minikube
* minikube start
* minikube docker-env -> copy and paste last line

### Build docker image
* build project
* docker build -t k8s-example:1.0 .

### Deploy MySql image
* kubectl apply -f mysql-ConfigMap.yaml
* kubectl apply -f mysql-secrets.yaml
* kubectl apply -f db-deployment.yaml

### Login to MySql
* kubectl get pods
* copy Myqsl pod name
* kubectl exec -it <pod_name> /bin/bash
* mysql -h mysql -u root -p
* enter password

### Show databases
* show databases;
* use <database_name>;

----------------
### Show tables
* show tables;
* you can use any sql statement
----------------

### Deploy app
* kubectl apply -f app-deployment.yaml

### Access Service
* kubectl get svc -> check NodePort
* minikube ip
* http://ip:nodeport

![img](https://github.com/geraldine999/K8S-Spring-Mysql-ConfigMap-Secret/assets/70971944/99cd8826-2c44-42b8-bf6d-98ef6124f424)


