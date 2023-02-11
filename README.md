# redis-sts

- https://rancher.com/blog/2019/deploying-redis-cluster/

# Deploy Redis Cluster
```
kubectl exec -it redis-cluster-0 -- redis-cli --cluster create --cluster-replicas 1 $(kubectl get pods -o=jsonpath='{range .items[*]}{.status.podIP}:6379 {end}')
```
