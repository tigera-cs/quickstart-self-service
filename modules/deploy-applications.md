# Deploy Applications

## `yaobank` Application

## `bookinfo` Application

## `hipstershop` Application

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