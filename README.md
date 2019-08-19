# go-app-in-kubernetes
kuberntetes poc using go app

Dependencies:
sudo minikube (minikube start —vm-driver=none)


Running
sudo kubectl apply -f deployment.yml 
sudo kubectl apply -f service.yml
sudo kubectl apply -f go-app-ingress.yml

echo "$(sudo minikube ip) kube.local" | sudo tee -a /etc/hosts


reference:
    1.kubctl
        i) https://www.digitalocean.com/community/tutorials/how-to-deploy-resilient-go-app-digitalocean-kubernetes
        ii) https://testdriven.io/blog/running-flask-on-kubernetes/
    3. helm charts
        i) https://daemonza.github.io/2017/02/20/using-helm-to-deploy-to-kubernetes/