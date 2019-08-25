# go-app-in-kubernetes
kuberntetes poc using go app

Dependencies:
sudo minikube (minikube start —vm-driver=none)


Running
sudo kubectl apply -f deployment.yml 
sudo kubectl apply -f service.yml
sudo kubectl apply -f go-app-ingress.yml

echo "$(sudo minikube ip) kube.local" | sudo tee -a /etc/hosts

Running using helm
helm init
helm install --name k8s-demo ./mychart --set service.type=NodePort

reference:
    1.kubctl
        i) https://www.digitalocean.com/community/tutorials/how-to-deploy-resilient-go-app-digitalocean-kubernetes
        ii) https://testdriven.io/blog/running-flask-on-kubernetes/
    2. helm charts
        i) https://daemonza.github.io/2017/02/20/using-helm-to-deploy-to-kubernetes/    
    3.running using helm
        i) https://docs.bitnami.com/kubernetes/how-to/create-your-first-helm-chart/