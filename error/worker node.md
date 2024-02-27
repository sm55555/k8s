


<img width="700" alt="스크린샷 2024-02-27 160116" src="https://github.com/sm55555/k8s/assets/38831314/a9e393b2-f141-4406-9b60-496eade55f8e">

위 그림과 같이 Worker node에서 pod 를 정상적으로 배포하려면


해당 예제에서는 컨테이너 런타임이 containerd이다. 아래 두 서비스가 정상적으로 켜져 있어야 pod 배포가 정상적으로 작동된다.

```
systemctl status kubelet
systemctl status containerd
```
