# high-u/docker-letsencrypt

## Usage

```
sudo docker network create hogenet
sudo docker-compose -f docker-compose.proxy.yaml up -d
sudo docker-compose -f app/docker-compose.nodered.yaml up -d
```

## Note

- docker-compose で ネットワーク作成すると、そのものずばりのネットワーク名を指定できないっぽいので、それが嫌で、外に出した。
- docker-compose v2 を使用しているのは、 v3 だと volumes_from が使えなかったから。volumes で代用できるが横着した。
