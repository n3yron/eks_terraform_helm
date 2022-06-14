cd eks
terraform init
terraform plan
terraform apply --auto-approve
aws eks --region <region> update-kubeconfig --name <cluster_name>
# Ingress
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.2.0/deploy/static/provider/aws/deploy.yaml