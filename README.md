# PresentWebProject

####docker CLI commands (power shell run as administrator)
docker --version
docker pull redis
docker run --name my-redis -d redis
docker exec -it my-redis redis-cli
SET name "Alice"
GET name
docker stop my-redis
exit
docker stop my-redis
docker rm my-redis
####Working with docker file
create dockerprojects\redis
git bash open the above folder
nano Dockerfile
FROM redis:latest
CMD ["redis-server"]
docker build -t redisnew .
docker run --name myredisnew -d redisnew
docker ps
docker stop myredisnew
docker login
docker ps -a
docker commit 028948c4429d rishitha12/redis
docker images
docker push rishitha12/redis
docker rm 028948c4429d
docker rmi rishitha12/redis
docker logout
=====================================
#minikube
minikube start
minikube ip
minikube kubectl -- get pods -A
kubectl create deployment mynginx --image=nginx
kubectl get deployments
kubectl get pods
kubectl describe pods
kubectl expose deployment mynginx --type=NodePort --port=80 --target-port=80
kubectl scale deployment mynginx --replicas=4
kubectl get service mynginx
kubectl port-forward svc/mynginx 8081:80
==========================================








