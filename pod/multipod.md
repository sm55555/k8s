### multipod

예제

```
apiVersion: v1
kind: Pod
metadata:
  name: sm55555-nginx-redis
  labels:
    app: nginx-redis
spec:
  containers:
  - name: nginx-container
    image: nginx
  - name: redis-container
    image: redis

```

로그를 볼때는 아래와 같은 규칙을 따른다.

```
kubectl logs [metadata] -c [containers.name]
kubectl logs sm55555-nginx-redis -c nginx-container
```


