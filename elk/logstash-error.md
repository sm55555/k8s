```
[2025-02-04T17:33:21, 599][ERROR)[logstash. .licensechecker. .licensereader] Unable to retrieve license information from license server
[:message: =>"Got response code 401° contacting Elasticsearch at URL https://elastic.com:9200/xpack"") 
```

발생 시

/etc/logstash/logstash.yml

```
xpack.monitoring.elasticsearc.username :
xpack.monitoring.elasticsearc.password :
```

값을 

logstash.conf의 output 절의 user, passwrod랑 맞춤
