```shell script
k3d cluster create my-cluster --volume /home/aaleksandrov/kuber-pv:/data --servers 3 --agents 2 --port "8081:80@loadbalancer" --port "8443:443@loadbalancer" --k3s-server-arg '--no-deploy=traefik'
helm install ingress-nginx ingress-nginx/ingress-nginx
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.3.1/aio/deploy/recommended.yaml
```