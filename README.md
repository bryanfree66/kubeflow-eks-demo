This is a demo of using KubeFlow on AWS EKS to automate the machine learning workflow. It is a work in progress.

EKS Setup
1. Install and configure the AWS CLI: shorturl.at/fjtxX
2. Install eksctl: shorturl.at/gvHP8
3. Intall kfctl: shorturl.at/ftHJS

KubeFlow Setup
1. To create the Kubernetes cluster, run:  **eksctl create cluster -f cluster/cluster.yaml
2. When the nodes become availiable, verify by running : **kubectl get nodes
3. Download the dashboard:  **wget https://api.github.com/repos/kubernetes-sigs/metrics-server/tarball/v0.3.6 tar zxvf v0.3.6
4. Install the dashboard: **kubectl apply -f kubernetes-sigs-metrics-server-d1f4f6f/deploy/1.8+
5. You can now delete the tar file from step 3
6. Verify metric server: **kubectl get deployment metrics-server -n kube-system
7. Deploy the recommended dashboard YAML:  **kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0-rc5/aio/deploy/recommended.yaml
8. Apply the admin service account YAML:  **kubectl apply -f service_account/eks-admin-service-account.yaml
9. 

Working...
