# kubectl commands

## kubectl current context
```shell
kubectl config current-context
```

## kubectl contexts
```shell
kubectl config get-contexts
```

## kubectl contexts
```shell
kubectl config use-context <context-name>
```

## kubectl list pods
```shell
kubectl get pods
```

## kubectl list pods
```shell
kubectl get pods
```

## kubectl port-forward 
```shell
kubectl port-forward -n <namespace> svc/<servicename> <port-forwarded>:<port-origin>
```

## kubectl get secret
first install:
winget install jqlang.jq
```shell
kubectl get secret <secret> -o json | jq '.data | map_values(@base64d)'
```
