### K9S 최신 버전 설치

```
K9S_VERSION=$(curl -s https://api.github.com/repos/derailed/k9s/releases/latest | jq -r '.tag_name')
curl -sL https://github.com/derailed/k9s/releases/download/${K9S_VERSION}/k9s_Linux_amd64.tar.gz | sudo tar xfz - -C /usr/local/bin k9s
```

### Metric-server 최신 버전 설치

반영되는데 조금 시간이 필요하다...

```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml

kubectl get deployment metrics-server -n kube-system

NAME             READY   UP-TO-DATE   AVAILABLE   AGE
metrics-server   1/1     1            1           6m
```

<img width="281" alt="image" src="https://github.com/sm55555/k8s/assets/38831314/059b4845-38c5-47a0-96bd-624f4312a3fb">

