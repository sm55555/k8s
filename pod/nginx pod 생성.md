
## [테스트 환경]

### master node(Ubuntu 20.04), worker node(Ubuntu 20.04)


k8s 서비스 확인

```
systemctl status kubelet
```

nginx yaml 파일 만들

#### pod.yml
```
apiVersion: v1
kind: Pod
metadata:
  name: nginx
  labels:
    app: nginx
spec:
  containers:
    - name: nginx-container
      image: nginx
```

적용
```
kubectl apply -f pod.yml
```

pod 확인
```
kubectl get pods -o wide
kubectl describe pod nginx
```
