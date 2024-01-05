# cubix-cloudnative-block3-homework

Miskovits Dániel

# installation / deployment commands

```
kubectl apply -f .\deployment-backapp.yaml
kubectl apply -f .\service-backapp.yaml
kubectl apply -f .\deployment-frontapp.yaml
kubectl apply -f .\service-frontapp.yaml
kubectl apply -f .\ingress.yaml
```

# command(s) for checking the logs of the backapp

```
kubectl logs deploy/backapp
```

# command for listing all frontapp related resources (1 command)

```
kubectl get all -l homework=frontapp
```

Note, that it will NOT include ingress.

# command for deleting both applications’ resources (1 command)

```
kubectl delete pod,replicaset,deploy,svc,ing -l training=block3
```
