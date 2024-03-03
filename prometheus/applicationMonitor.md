## applicationMonitor

k8s 환경에서 최신 application들은 자동적으로 prometheus가 설치되어서 나오는 경우도 있지만, nginx 같은 경우에는 따로 없어서 adapter 형식으로 /metric을 노출 시켜줘야 모니터링 가능하다.
