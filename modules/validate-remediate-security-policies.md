# Validate Remediated Security Policies

## `monitoring` to `hipstershop`

The `monitoring` to `hipstershop` flow is now permitted by the below security policies.

### Egress

- The `monitoring` security policy in the `platform` tier

### Ingress

- The `frontend` security policy in the `appsec` tier

> Remediated `monitoring` to `hipstershop` Service Graph view

![sg-monitoring-hipstershop-gif](images/sg-monitoring-hipstershop.gif)

## `monitoring` to `yaobank`

The `monitoring` to `yaobank` flow is now permitted by the below security policies.

### Egress

- The `monitoring` security policy in the `platform` tier

### Ingress

- The `tenant-1-yaobank-allow` security policy in the `application` tier

> Remediated `monitoring` to `yaobank` Service Graph view

![sg-monitoring-yaobank-gif](images/sg-monitoring-yaobank.gif)

## `monitoring` to `bookinfo`

The `monitoring` to `bookinfo` flow is now permitted by the below security policies

### Egress

- The `monitoring` security policy in the `platform` tier

### Ingress

- The `tenant-2-bookinfo-allow` security policy in the `application` tier

> Remediated `monitoring` to `bookinfo` Service Graph view

![sg-monitor-bookinfo-gif](images/sg-monitor-bookinfo.gif)


## `loadgeneratorv2` to `frontend` in the `hipstershop` namespace

The `loadgeneratorv2` to `frontend` flow in the `hipstershop` namespace is now permitted by the below security policies

### Egress

- The `loadgenerator` security policy in the `appsec` tier

### Ingress

- The `loadgenerator` security policy in the `appsec` tier

> Remediated `loadgeneratorv2` to `frontend`  Service Graph view

![sg-loadgeneratorv2-frontened-gif](images/loadgeneratorv2-frontend.gif)

## `ratings` to `www.github.com`

The `ratings` to `www.github.com` flow is now permitted by the below security policies

### Egress

- The `tenant-2-bookinfo-allow` security policy in the `application` tier

### Ingress

- **Note** that there is no ingress security policy since the destination is external to the cluster. 

> Remediated `ratings` to `www.github.com` Service Graph view

![sg-ratings-github-gif](images/ratings-github.gif)