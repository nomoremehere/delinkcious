# Link Service

The link microservice. It uses a multi-stage [Dockerfile](Dockerfile) to generate a lean and mean image from SCRATCH that just includes the Go binary. The system has a CI/CD pipeline, but you also


## Build Docker image

```
$ docker build . -t farshidgilak/delinkcious-link-manager:${VERSION}
```

## Push to Registry

This will go by default to DockerHub. Make sure you're logged in:

```
$ docker login
```

Then push your image:

```
$ docker push farshidgilak/delinkcious-link-manager:${VERSION}
```

## Deploy to active Kubernetes cluster

If you want to push a local minikube make sure your kuectl is pointed to the right cluster and type:

```
$ kubectl apply -f k8s
```







