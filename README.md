


# Redis Master

git clone https://github.com/aliouba/k8sgettingstarted.git

cd k8sgettingstarted/guestbook/

kubectl create -f redis-master-deployment.yaml

# Expose Redis Master

kubectl create -f redis-master-service.yaml

# Redis Slave and Frontend

kubectl create -f redis-slave-deployment.yaml

kubectl create -f redis-slave-service.yaml

kubectl create -f frontend-deployment.yaml

kubectl create -f frontend-service.yaml

(Optional) kubectl scale deploy frontend --replicas 2
