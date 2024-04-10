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
