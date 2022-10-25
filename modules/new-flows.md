# Introduce New Flows

In this lesson a `monitoring-pod` will be deployed to query the `productpage`, `frontend`, and  `customer` microservices of the `bookinfo`, `hipstershop`, and `yaobank` namespaces respectively. 

`kubectl create namespace monitoring`

## `monitoring` to `hipstershop`

![new-flow-frontend.gif](images/new-flow-frontend.gif)

## `monitoring` to `bookinfo`

![new-flow-productpage.gif](images/new-flow-productpage.gif)

## `monitoring` to `yaobank`

![new-flow-yaobank.gif](images/new-flow-customer.gif)