# kubernetes-masterclass



# Generate password on base64
echo -n 'password' | base64


# Ingress Deployment
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml

kubectl get services -o wide -w -n ingress-nginx

# Cert Deployment
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.11.0/cert-manager.yaml


# Deploy Wordpress Stack

kubectl apply -k .
