# Introduce New Flows

In this lesson new flows will be introduced to the cluster. The objective is to observe which security policies will deny these flows and understand how the flows can be allowed in subsequent lessons.

# Deploy `monitoring-pod`

A `monitoring-pod` deployed in the `monitoring` namespace will be used to target the the `productpage`, `frontend`, and  `customer` microservices of the `bookinfo`, `hipstershop`, and `yaobank` namespaces respectively. 

> The `monitoring-pod` 

![new-flows-monitoring.gif](images/new-flow-monitoring.png)

Follow the below steps to deploy the `monitoring-pod` and iniate `curl` to the `productpage`, `frontend`, and  `customer` microservices.

```bash
kubectl run monitoring-pod --namespace monitoring -i --tty --image nicolaka/netshoot -- /bin/bash

while sleep 1;
do 
curl http://frontend.hipstershop.svc.cluster.local 
curl http://customer.yaobank.svc.cluster.local 
curl http://productpage.bookinfo.svc.cluster.local:9080
done
```

### `monitoring` to `hipstershop`

Observe the `Policies Board` to identify the security policy that would deny traffic from the `monitoring` namespace to the `hipstershop` namespace. 

![new-flow-frontend.gif](images/new-flow-frontend.gif)

### `monitoring` to `bookinfo`

Observe the `Policies Board` to identify the security policy that would deny traffic from the `monitoring` namespace to the `bookinfo` namespace. 

![new-flow-productpage.gif](images/new-flow-productpage.gif)

### `monitoring` to `yaobank`

Observe the `Policies Board` to identify the security policy that would deny traffic from the `monitoring` namespace to the `yaobank` namespace. 

![new-flow-yaobank.gif](images/new-flow-customer.gif)

# Deploy `monitoring-pod`