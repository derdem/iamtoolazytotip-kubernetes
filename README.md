# iamtoolazytotip-kubernetes

## useful commands

### minikube
- `minikube start`
- `minikube dashboard`
- `minikube service <service-name>` - opens the service in the browser
    - `minikube service iamtoolazytotip-api-server`
- `minikube stop`
- `minikube delete`

### kubectl

- `kubectl apply -f ./deployments/iamtoolazytotip-api-server-deployment.yml`
- `kubectl expose deployment iamtoolazytotip-api-server`

## Working with local docker images

Before running the docker build (oder docker compose build) command the following command must be executed: `eval $(minikube docker-env)`.
Then in the same terminal the docker build command can be executed. Deployment files need to have the imagePullPolicy set to Never.
Then locally built images can be used.