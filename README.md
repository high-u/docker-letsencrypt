# high-u/docker-letsencrypt

## Usage

```
sudo docker network create hogenet
sudo docker-compose -f docker-compose.proxy.yaml up -d
sudo docker-compose -f app/docker-compose.nodered.yaml up -d
```

## Note

- docker-compose で ネットワーク作成すると、そのものずばりのネットワーク名を指定できないっぽいので、それが嫌で、外に出した。
- docker-compose v2 を使用しているのは、 v3 だと volumes_from が使えなかったから。volumes で問題無いようだが横着した。
- let's encrypt の SSL 証明書の取得には下記のような制限があるので注意。
  - 20 certificates per registered domain per week (up from 5).
  - Added an exception to this limit for renewing certificates (issuing a new certificate with same names as a previous one).
  - Added a new limit on issuing certificates with the exact same set of names: 5 certificates per FQDN set per week.
