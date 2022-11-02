# Deploy Applications

> ### Quick Access - [Lesson Lab Tasks](#Lesson-Lab-Tasks) 

## `tenant-1 hipstershop` Application

### Pods
```bash
tigera@amp ~ % kubectl get pods -n hipstershop 
NAME                                     READY   STATUS    RESTARTS   AGE
adservice-78699c67f4-dsshz               1/1     Running   0          8d
cartservice-85c8fb75b4-zxhgn             1/1     Running   0          8d
checkoutservice-8d688cc8d-kts9l          1/1     Running   0          8d
currencyservice-6659fd6464-7j5tt         1/1     Running   0          8d
emailservice-5b7b99447d-kbkhz            1/1     Running   0          8d
frontend-58cf64dbb7-z4xmd                1/1     Running   0          8d
loadgenerator-777874bfb8-9xvn6           1/1     Running   0          8d
paymentservice-76b6cd7f8-n99cb           1/1     Running   0          8d
productcatalogservice-8d579645b-tt847    1/1     Running   0          8d
recommendationservice-66ddf76bb8-pn4zc   1/1     Running   0          8d
redis-cart-68579dffcd-wbx5x              1/1     Running   0          8d
shippingservice-7f6f45cf4-vhnxw          1/1     Running   0          8d
```

### Services

```bash
tigera@amp ~ % kubectl get services -n hipstershop
NAME                    TYPE           CLUSTER-IP     EXTERNAL-IP    PORT(S)        AGE
adservice               ClusterIP      10.0.125.138   <none>         9555/TCP       8d
cartservice             ClusterIP      10.0.238.82    <none>         7070/TCP       8d
checkoutservice         ClusterIP      10.0.77.47     <none>         5050/TCP       8d
currencyservice         ClusterIP      10.0.171.148   <none>         7000/TCP       8d
emailservice            ClusterIP      10.0.253.243   <none>         5000/TCP       8d
frontend                ClusterIP      10.0.122.196   <none>         80/TCP         8d
paymentservice          ClusterIP      10.0.195.250   <none>         50051/TCP      8d
productcatalogservice   ClusterIP      10.0.133.139   <none>         3550/TCP       8d
recommendationservice   ClusterIP      10.0.197.145   <none>         8080/TCP       8d
redis-cart              ClusterIP      10.0.127.118   <none>         6379/TCP       8d
shippingservice         ClusterIP      10.0.30.23     <none>         50051/TCP      8d
```

## `tenant-1 yaobank` Application

### Pods

```bash
tigera@amp ~ % kubectl get pods -n yaobank
NAME                        READY   STATUS    RESTARTS   AGE
customer-687b8d8f74-kjrw8   1/1     Running   0          9d
database-545f6d6d95-xt4kw   1/1     Running   0          9d
summary-7579bd9566-shm7c    1/1     Running   0          26d
summary-7579bd9566-vx95t    1/1     Running   0          9d
```

### Services


## `tenant-2 bookinfo` Application

### Pods

```bash
tigera@amp ~ % kubectl get pods -n bookinfo
NAME                              READY   STATUS    RESTARTS   AGE
details-v1-5498c86cf5-n7rj8       1/1     Running   0          12d
productpage-v1-65b75f6885-l7n5p   1/1     Running   0          12d
ratings-v1-b477cf6cf-q7st8        1/1     Running   0          12d
reviews-v1-79d546878f-nkkv2       1/1     Running   0          12d
reviews-v2-548c57f459-wdz99       1/1     Running   0          12d
reviews-v3-6dd79655b9-fjt5b       1/1     Running   0          12d
```

### Services

```bash
tigera@amp ~ % kubectl get services -n bookinfo
NAME          TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)    AGE
details       ClusterIP   10.0.51.237    <none>        9080/TCP   26d
productpage   ClusterIP   10.0.119.151   <none>        9080/TCP   26d
ratings       ClusterIP   10.0.23.19     <none>        9080/TCP   26d
reviews       ClusterIP   10.0.235.15    <none>        9080/TCP   26d
```

# Lesson Lab Tasks

### Apply manifest to deploy namespaces and applications

```yaml
kubectl apply -f apps/namespaces.yaml
kubectl apply -f apps/hipstershop.yaml
kubectl apply -f apps/yaobank.yaml
kubectl apply -f apps/bookinfo.yaml
```

# Lesson Video