# django-k8s

https://www.youtube.com/watch?v=NAOsLaB6Lfc

cd /web
gunicorn --bind 0.0.0.0:8000 django_k8s.wsgi:application

export KUBECONFIG=~django-k8s-kubeconfig.yaml
echo $KUBECONFIG

kubectl apply -f k8s/nginx/deployment.yaml

kubectl exec -it <podname> -- /bin/bash

E0807 05:48:05.029373   12065 memcache.go:265] couldn't get current server API group list: Get "http://localhost:8080/api?timeout=32s": dial tcp 127.0.0.1:8080: connect: connection refused
The connection to the server localhost:8080 was refused - did you specify the right host or port?


https://github.com/codingforentrepreneurs/iac-python