# es-demo
---
docker run elastic/rally list tracks
docker run elastic/rally race --track=nyc_taxis --test-mode --pipeline=benchmark-only --target-hosts=:9200

kubectl apply -f rally.yaml
kubectl -n elk exec -it esrally -- /bin/sh
esrally race --track=nyc_taxis --pipeline=benchmark-only --challenge=append-no-conflicts-index-only --target-hosts=10.108.39.115:9200

#Appendix - Auxiliary commands

esrally race --track=nyc_taxis --pipeline=benchmark-only --challenge=append-no-conflicts-index-only --target-hosts=10.108.39.115:9200 --client-options="use_ssl:false,verify_certs:false"

curl -i -X POST http://elastic:changeme@10.108.39.115:9200/_cluster/nodes/


curl -X GET "elastic:changeme@10.108.39.115:9200/_cat/indices/my-index-*?v=true&s=index&pretty"

curl -X PUT "elastic:changeme@10.108.39.115:9200/my-index-000001?pretty"

curl -X POST "10.105.185.13:9200/_security/_authenticate?pretty"