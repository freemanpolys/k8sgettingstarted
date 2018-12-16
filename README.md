# dakar-innovation-day

[Demo docker](https://github.com/aliouba/flask-docker)

[Demo docker with CI/CD](https://github.com/aliouba/ci-jenkins-demo)

# Redis Master

git clone https://github.com/aliouba/dakar-innovation-day.git

cd guestbook/

kubectl create -f redis-master-deployment.yaml

# Expose Redis Master

kubectl create -f redis-master-service.yaml

# Redis Slave and Frontend

kubectl create -f redis-slave-deployment.yaml

kubectl create -f redis-slave-service.yaml

kubectl create -f frontend-deployment.yaml

kubectl create -f frontend-service.yaml

(Optional) kubectl scale deploy frontend --replicas 4

# Create Mysql database

cd ../dakar-innovation-day

kubectl create -f wordpress-demo/mysql/

# Create Wordpress instance

kubectl create -f wordpress-demo/wordpress/

# Create Ingress resource

kubectl delete -f wordpress-demo/wordpress/

kubectl delete -f wordpress-demo/mysql/

kubectl create -f wordpress-demo/mysql/

kubectl create -f wordpress-demo/wordpress-ing/


