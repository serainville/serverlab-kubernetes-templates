# MySQL Dump Kubernetes CronJob


## Building the Docker Image

```
docker build -t mysqldump .
```

## Push Image to Google Container Registery (gcr.io)
Add a new tag to the Docker image. The tag must start with the address of the container registry, which
is `gcr.io` in this example.

```
docker tag mysqldump gcr.io/serverlab/mysqldump-demo:0.0.1
```

Push the newly tagged image up to Google Container Registry
```
docker push gcr.io/serverlab/mysqldump-demo:0.0.1
```
