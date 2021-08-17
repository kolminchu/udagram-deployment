# udagram-deployment


 # creating deployment
kubectl apply -f udagram-configmap.yml
kubectl apply -f udagram-secret.yml
kubectl apply -f aws-secret.yml
kubectl apply -f feedapi-deployment.yml
kubectl apply -f feedapi-service.yml
kubectl apply -f usersapi-deployment.yml
kubectl apply -f usersapi-service.yml
kubectl apply -f revproxy-deployment.yml
kubectl apply -f revproxy-service.yml
kubectl apply -f frontend-deployment.yml
kubectl apply -f frontend-service.yml


  # deleting deployment
kubectl delete -f udagram-configmap.yml
kubectl delete -f udagram-secret.yml
kubectl delete -f aws-secret.yml
kubectl delete -f feedapi-deployment.yml
kubectl delete -f feedapi-service.yml
kubectl delete -f usersapi-deployment.yml
kubectl delete -f usersapi-service.yml
kubectl delete -f revproxy-deployment.yml
kubectl delete -f revproxy-service.yml
kubectl delete -f frontend-deployment.yml
kubectl delete -f frontend-service.yml
kubectl delete -f frontend-service.yml


  # change the image of the deployment

kubectl set image deployment <deployment_name> <container_name>=<docker_hub_user_account>/<image_name>:<tag>

kubectl set image deployment udagram-feed-api-deployment udagram-feed-api=scharati/udagram-api-feed:v1
kubectl set image deployment udagram-users-deployment udagram-api-users=scharati/udagram-api-users:v1
kubectl set image deployment rev-proxy-deploy rev-proxy=scharati/rev-proxy:v1
kubectl set image deployment udagram-frontend-deployment udagram-frontend=scharati/udagram-frontend:v1












