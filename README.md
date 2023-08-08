# django-k8s

https://www.youtube.com/watch?v=NAOsLaB6Lfc

cd /web
gunicorn --bind 0.0.0.0:8000 django_k8s.wsgi:application

export KUBECONFIG=~django-k8s-kubeconfig.yaml
echo $KUBECONFIG

kubectl apply -f k8s/nginx/deployment.yaml

kubectl exec -it <podname> -- /bin/bash

https://github.com/codingforentrepreneurs/iac-python

docker login registry.digitalocean.com

dop_v1_936a471ea4dd904dce7334fe9ef1b35be4d845801551bb61138be855dd3cd7eb

docker image push --all-tags registry.digitalocean.com/django--k8s/django-k8s

kubectl create secret generic django-k8s-web-prod-env --from-env-file=web/.env.prod

DIFERENÇAS:
kubectl get nodes (Não está pegando os nodes no cluster na digital ocean)

kubectl get secrets (Não tem os dois secrests padrão 2:53:30)