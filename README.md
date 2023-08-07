# django-k8s

https://www.youtube.com/watch?v=NAOsLaB6Lfc

cd /web
gunicorn --bind 0.0.0.0:8000 django_k8s.wsgi:application

export KUBECONFIG=~django-k8s-kubeconfig.yaml
echo $KUBECONFIG