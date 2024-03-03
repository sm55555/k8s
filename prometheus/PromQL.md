### PromQL

필요한 Label을 이용하여 검색이 가능하다.

node가 m-k8s 인것만

```
node_memory_Active_bytes{node="m-k8s"}
```

node가 m-k8s이 아닌것만

```
node_memory_Active_bytes{node="m-k8s"}
```

<img width="1274" alt="image" src="https://github.com/sm55555/k8s/assets/38831314/ec16ad1f-45b1-41a7-a62a-6c30f6cd610b">


어느 pod가 몇번 Restart 되었는지 확인

```
kube_pod_container_status_restarts_total > 6
```

<img width="1280" alt="image" src="https://github.com/sm55555/k8s/assets/38831314/0fd6513d-c12e-42ad-8a74-5b8ef99b5b7e">
