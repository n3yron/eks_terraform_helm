# Create EKS cluster via TF
cd eks
terraform init
terraform plan
terraform apply --auto-approve
aws eks --region <region> update-kubeconfig --name <cluster_name>
# Ingress
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.2.0/deploy/static/provider/aws/deploy.yaml
# Install
helm install app n3yron 8080
# Check:
curl a20de3f0c1ded4a23b0746e06f3c6b1b-1500600435.us-east-2.elb.amazonaws.com:8080
curl a20de3f0c1ded4a23b0746e06f3c6b1b-1500600435.us-east-2.elb.amazonaws.com:8080/health
curl https://n3yron.nebula.video/
curl https://n3yron.nebula.video/health