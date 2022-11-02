# Create Ingress Resources for Application

> ### Quick Access - [Lesson Lab Tasks](#Lesson-Lab-Tasks) 

![ingress](images/ingress.png)

## Create ingress for `hipstershop`

The following manifest will create an ingress resource for the `frontend` deployment in the `hipstershop` namespace. 

> ingress-frontend manifest

```yaml
  apiVersion: networking.k8s.io/v1
  kind: Ingress
  metadata:
    name: ingress-frontend
    namespace: hipstershop
  spec:
    ingressClassName: nginx
    rules:
      - host: www.hipstershop.com
        http:
          paths:
            - pathType: Prefix
              backend:
                service:
                  name: frontend
                  port:
                    number: 80
              path: /
```

```bash
tigera@amp ~ % kubectl get ingress -n hipstershop
NAME               CLASS   HOSTS                 ADDRESS         PORTS   AGE
ingress-frontend   nginx   www.hipstershop.com   20.221.88.154   80      29d
```



## Create ingress for `yaobank`

> ingress-customer manifest

```yaml
  apiVersion: networking.k8s.io/v1
  kind: Ingress
  metadata:
    name: ingress-customer
    namespace: yaobank
  spec:
    ingressClassName: nginx
    rules:
      - host: www.yaobank.com
        http:
          paths:
            - pathType: Prefix
              backend:
                service:
                  name: customer
                  port:
                    number: 80
              path: /
```

```bash
tigera@amp ~ % kubectl get ingress -n yaobank    
NAME              CLASS   HOSTS             ADDRESS         PORTS   AGE
ingress-yaobank   nginx   www.yaobank.com   20.221.88.154   80      29d
```

## Create ingress for `bookinfo`

```yaml
  apiVersion: networking.k8s.io/v1
  kind: Ingress
  metadata:
    name: ingress-productpage
    namespace: bookinfo
  spec:
    ingressClassName: nginx
    rules:
      - host: www.bookinfo.com
        http:
          paths:
            - pathType: Prefix
              backend:
                service:
                  name: productpage
                  port:
                    number: 9080
              path: /
```

```bash
tigera@amp ~ % kubectl get ingress -n bookinfo
NAME                  CLASS   HOSTS              ADDRESS         PORTS   AGE
ingress-productpage   nginx   www.bookinfo.com   20.221.88.154   80      29d
```
![request-bookinfo](images/request-bookinfo.png)

![bookinfo](images/bookinfo.png)

## Create ingress for `bookinfo`

> Service Graph - Ingress Namespace

![sg-ingress-ns](images/sg-ingress-ns.png)

# Lesson Lab Tasks

### Deploy and validate ingress resources

```bash
kubectl apply -f ingress/hipstershop.yaml
kubectl apply -f ingress/yaobank.yaml
kubectl apply -f ingress/bookinfo.yaml
```

```bash
kubectl get ingress -n hipstershop 
kubectl get ingress -n yaobank 
kubectl get ingress -n bookinfo
```


# Lesson Video