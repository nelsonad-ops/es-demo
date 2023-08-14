esrally.md

yum install gcc -y
yum install make -y
yum install python3 -y
python3 -m pip install --user esrally
python3 -m pip install --user --upgrade pip

curl https://pyenv.run | bash
pyenv install 3.8.16
vi ~/.bashrc
export PYENV_ROOT="$HOME/.pyenv"
command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
bash



python3 -m pip install esrally


---
docker run elastic/rally list tracks
$ docker run elastic/rally race --track=nyc_taxis --test-mode --pipeline=benchmark-only --target-hosts=:9200

kubectl run -it --generator "run-pod/v1" esrally --image elastic/rally -- /bin/sh
esrally race --track=nyc_taxis --pipeline=benchmark-only --challenge=append-no-conflicts-index-only --target-hosts=10.106.17.121:9200 --client-options="use_ssl:true,verify_certs:false,basic_auth_user:'elastic'"

curl -i -X POST http://elastic:changeme@elasticsearch.elk.svc.cluster.local:9200/_cluster/nodes/


curl -X GET "elastic:changeme@10.106.17.121:9200/_cat/indices/my-index-*?v=true&s=index&pretty"

curl -X PUT "elastic:changeme@10.106.17.121:9200/my-index-000001?pretty"

curl -X POST "10.105.185.13:9200/_security/_authenticate?pretty"

