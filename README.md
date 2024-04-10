Navigate into the frontend directory, and confirm the presence of the `docker-compose.deploy.yml` file:

```
cd frontend
ls -la
```

### Step 1.
Create a new Docker network and name it ```micro_network```:
```
docker network create micro_network
```
### Step 2.
Build each of the microservice Docker container images:
```
docker-compose -f docker-compose.deploy.yml up -d
docker images
```

### Step 3.
Launch the microservice environment:
```
docker-compose -f docker-compose.deploy.yml build
docker ps -a
```

### Step 4.
Prepare each microservice mysql database:
```
 docker exec -it corder-service flask db init
 docker exec -it corder-service flask db migrate
 docker exec -it corder-service flask db upgrade
 docker exec -it cproduct-service flask db init
 docker exec -it cproduct-service flask db migrate
 docker exec -it cproduct-service flask db upgrade


```
