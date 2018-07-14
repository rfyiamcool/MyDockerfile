# ETCD

register & discovery for test ...

### How

> one node

```
docker run \
  -d \
  -p 2379:2379 \
  -e 'ETCD_ADVERTISE_CLIENT_URLS=http://xx.xx.xx.xx:2379' \
  --name some-etcd \
  rfyiamcool/etcd:latest
```

> create cluster in cluster

```
docker service create \
  --name etcd \
  -e 'CLUSTER_SIZE=3' \
  -e 'ETCD_ADVERTISE_CLIENT_URLS=http://xx.xx.xx.xx:2379,http://xx.xx.xx.xx:2379' \
  --replicas=3 \
  --publish 2379:2379
  --network=etcd \
  rfyiamcool/etcd:latest
```
