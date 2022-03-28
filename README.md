# Sample Application

The repository contains a simple Golang based application. The application used to demonstrate
deployment and promotion process following GitOps methodology using various GitOps tools.

## Build and Run

To run application locally use the following command:

```
go run ./main.go

Go to http://localhost:8080/
```

## Make a Change

To make a sample change run the following command:

```
sed -i '' 's/const name = "Golang"/const name = "GitOps"/' main.go
```

## Publish and Deploy

To publish the docker image use the following command:

```
docker build -t genedocker/gitops-demo-app:v0.1 .
docker build -t genedocker/gitops-demo-app:v0.2 .
```

Two application versions are available in Docker Hub:

* genedocker/gitops-demo-app:v0.1
* genedocker/gitops-demo-app:v0.2

To deploy the application use deployment manifests stored in https://github.com/genekuo-org/gitops-demo-deployment
