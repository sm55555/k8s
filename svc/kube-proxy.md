## kube-proxy

### iptables (현재 방식)

- default kubernetes network mode
- kube-proxy는 service API (Cluser IP, Nodeport 생성 시) iptables rule이 생성
- 클라이언트 연결은 kube-proxy가 받아서 iptables 룰을 통해 연결

노드 별로 iptables가 존재한다. EKS 경우 접속해서 아래 명령어로 확인이 가능하다.
```
[root@ip-172-1-1-1 ec2-user]# iptables -t nat -S | grep 80
-A KUBE-SERVICES -d 10.100.29.175/32 -p tcp -m comment --comment "default/loadbalaner-service cluster IP" -m tcp --dport 80 -j KUBE-SVC-AAAAAAAAAAAA
-A KUBE-SERVICES -d 10.100.42.210/32 -p tcp -m comment --comment "default/sm55555-svc:http cluster IP" -m tcp --dport 80 -j KUBE-SVC-AAAAAAAAAAAA
```
