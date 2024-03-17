Beyla Demo
----------

Create a Kubernetes cluster

```
kind create cluster --config=kind.yaml
```

Install the demo apps (Nginx, Java service, Rust service, Go service, load generator)

```
kubectl apply -f demo-apps.yaml
```

Port forward the nginx service

```
kubectl port-forward services/nginx 3333:3333
```

Generate load

```
./loadgen.sh
```
