# Using Service Graph to Identify Denied Flows

![sg-deny-gif](images/sg-block-flows.gif)

## Denied flow from `monitoring-pod`

### `monitoring` to `hipstershop`

The `monitoring` to `hipstershop` flow is denied by the below security policy.

### Ingress

- The `tenant-1-restrict` security policy in the `security` tier.

### Service Graph View

> Denied `monitoring` to `hipstershop` Service Graph

![sg-monitoring-hipstershop-deny-gif](images/sg-monitoring-hipstershop-deny.gif)

### `monitoring` to `yaobank`

The `monitoring` to `yaobank` flow is denied by the below security policy.

### Ingress

- The `tenant-1-restrict` security policy in the `security` tier.

### Service Graph View

> Denied `monitoring` to `yaobank` Service Graph

![sg-monitor-yaobank-deny-gif](images/sg-monitoring-yaobank-deny.gif)

### `monitoring` to `bookinfo`

The `monitoring` to `bookinfo` flow is denied by the below security policy.

### Ingress

- The `tenant-2-restrict` security policy in the `security` tier.

> Denied `monitoring` to `bookinfo` Service Graph

![sg-monitoring-bookfino-deny-gif](images/sg-monitoring-bookinfo-deny.gif)

## Denied flow from `loadgeneratorv2`

The `loadgeneratorv2` to `frontend` flow in the `hipstershop` namespace is denied by the below security policy.

### Egress

- The `tenant-1-default-deny` security policy in the `default` tier. 

> Denied `loadgeneratorv2` to `frontend` Service Graph

![sg-loadgeneratorv2-deny-gif](images/sg-loadgeneratorv2-deny.gif)

## Denied flow from `ratings`

The `ratings` to `www.github.com` flow is denied by the below security.

### Egress

- The `tenant-2-bookinfo-allow` security policy in the `application` tier. 

> Denied `ratings`  to `www.github.com` Service Graph

![sg-ratings-deny-gif](images/sg-ratings-deny.gif)

# Lesson Video

[![sg-denied-flows](images/sgdd.png)](https://tigera.wistia.com/medias/88j386d49p)