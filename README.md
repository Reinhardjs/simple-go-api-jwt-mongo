## Simple GO API 

<!-- ABOUT THE PROJECT -->

![image](https://user-images.githubusercontent.com/7758970/204043976-feed56b2-eca0-4de0-9b06-1ec42848bfe0.png)

I've deployed this project to my personal VPS, and deployed to `single-node kubernetes`

You can access via http://103.134.154.18:32012

## Credentials
```
# Here are the user credentials to access `GET /token` endpoint to get the jwt-token
1. ADMIN
{
    "email": "admin@email.com",
    "password": "password"
}

2. USER
{
    "email": "user@email.com",
    "password": "password"
}
```

<br>

Your token will be expiring for 3 minutes. You should request for new token from `GET /token` endpoint <br>
You can use non expiring token below, if u disturbed by the expired token

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJVc2VySWQiOiI2MzgwYzIxNmE2NjBhOWQ3ZjRmMDZmZDIiLCJFbWFpbCI6ImFkbWluQGVtYWlsLmNvbSIsIlJvbGUiOiJhZG1pbiJ9.kkcnAqajjcx0YmtRnWk-P594v_2wIEObwUzTtuMq_JY


#### Built With

* Go (Mux, JWT)
* Docker
* Kubernetes
* MongoDB


<!-- GETTING STARTED -->
## Getting Started


### Prerequisites

This project is configured to be able to containerized using docker (Dockerfile). And deployed on a single-node kubernetes cluster. (Deployment.yaml)

Here is what i mean by single-node cluster, go checkout my story on medium here:

https://reinhardjsilalahi.medium.com/beginners-guide-simple-hello-kubernetes-all-in-one-on-a-single-vps-fcfdfee9edfc

Below is the commands to deploy the changes to the pod

```sh
git pull
```

```sh
docker build -t simple-api .
```

```sh
kubectl apply -f Deployment.yaml
```

```sh
kubectl rollout restart deployment/simple-api
```


<!-- USAGE EXAMPLES -->
## Usage
You can see the example usages from `swagger.yml` and open it on https://editor.swagger.io

Our you can import the postman request collection, `simple-api.postman_collection.json`
