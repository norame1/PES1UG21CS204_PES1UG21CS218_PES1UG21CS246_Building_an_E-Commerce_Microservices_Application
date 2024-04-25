# Project 6: Building an E-commerce Microservices Application on Cloud using Docker, Kubernetes, Jenkins, and Git
NOTE: Replace the MongoDB Atlas Cluster URL with your own generated Cluster URL. 
<br/>
Team Number: 2
<br/>
Name: GAUTAM_HARI_JESHWANTH
<br/>
SRN: PES1UG21CS204_PES1UG21CS218_PES1UG21CS246_Building_an_E-Commerce_Microservices_Application

WEEK1:

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
