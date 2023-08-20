## Ingress란

- HTTP나 HTTPS를 통해 클러스터 내부의 서비스를 외부로 노출하기 위해 사용한다.
- 기능
  1. Service에 외부 URL을 제공
  2. 트래픽을 로드밸런싱
  3. SSL 인증서 처리
  4. Virtual hosting을 지정

<img width="658" alt="image" src="https://github.com/sm55555/k8s/assets/38831314/86b9cd9a-156a-47c7-971a-479ee85bd761">

pod들의 진입점을 Service 예를들어 ClusterIP로 묶어주고 그 ClusterIP 들의 진입점을 알맞은 Ingress Rule을 통해 Ingress Controller가 관리하며 분배해준다.

하지만 기본 Ingress Controller 기본 템플릿에서는 NodePort역할까지 하므로... 클라이언트 -> NodePort:30200 으로 밖에 못온다.

추가해야할 부분 앞에 LB 붙여서 서비스 하는것 !
