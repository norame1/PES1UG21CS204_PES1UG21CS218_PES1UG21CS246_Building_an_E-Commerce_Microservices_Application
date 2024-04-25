# Project 6: Building an E-commerce Microservices Application on Cloud using Docker, Kubernetes, Jenkins, and Git
 
<br/>
Team Number: 2
<br/>
Name: GAUTAM_HARI_JESHWANTH
<br/>
SRN: PES1UG21CS204_PES1UG21CS218_PES1UG21CS246_Building_an_E-Commerce_Microservices_Application

Building docker containers:

```bash
docker build -t tradetrove-frontend ./frontend
docker tag tradetrove-frontend gautamsanthosh/tradetrove-frontend:latest
docker push gautamsanthosh/tradetrove-frontend:latest
docker build -t tradetrove-auth ./authenticate
docker tag tradetrove-auth gautamsanthosh/tradetrove-auth:latest
docker push gautamsanthosh/tradetrove-auth:latest
docker build -t tradetrove-cart ./cart
docker tag tradetrove-cart gautamsanthosh/tradetrove-cart:latest
docker push gautamsanthosh/tradetrove-cart:latest
docker build -t tradetrove-items ./items
docker tag tradetrove-items gautamsanthosh/tradetrove-items:latest
docker push gautamsanthosh/tradetrove-items:latest
docker build -t tradetrove-order ./order
docker tag tradetrove-order gautamsanthosh/tradetrove-order:latest
docker push gautamsanthosh/tradetrove-order:latest

```
Kubernetes:

```bash
kubectl delete deployments --all
kubectl delete services --all
kubectl apply -f ./k8s/
kubectl get pods
```

Running jenkins:
```bash
docker build . -t jenkins
docker run -p 8080:8080 -p 50000:50000 -it jenkins
```
Port Forwarding:
```bash
kubectl port-forward auth-deployment-687c7fcb4-xrszj 5000:5000
kubectl port-forward cart-deployment-67966b9669-8clwq 5001:5001
kubectl port-forward frontend-deployment-65c645798d-zczln 3000:3000
kubectl port-forward items-deployment-585c9c5b-nl6fj 5002:5002
kubectl port-forward order-deployment-d96545469-gqkwk 5003:5003
```
