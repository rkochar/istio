# Istio

```
minikube start --memory=16384 --cpus=4 -p istio

istioctl install
kubectl label ns default istio-injection=enabled

kubectl apply -f ./addons/prometheus.yaml
kubectl apply -f ./addons/jaeger.yaml
kubectl apply -f ./addons/kiali.yaml

kubectl apply -f ./custom-routing/
```

To test,
```
sudo minikube tunnel -p istio
curl localhost
```
