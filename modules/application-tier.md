# The Application Tier

![yaobank-allow](images/application-tier.png)

## `yaobank-allow` Security Policy

The `yaobank-allow` security policy will have rules to permit ingress and egress traffic flows to and from the endpoints in the namespace. All endpoints in the yaobank namespace will be able to send and receive traffic from all other endpoints in the same namespace. Traffic flows entering and leaving the namespace must be explicitly permitted using policy rules.  

> yaobank-allow security policy

![yaobank-allow](images/yaobank-allow.png)

> bookinfo-allow security policy

## `bookinfo-allow` Security Policy

The `bookinfo-allow` security policy will have rules to permit ingress and egress traffic flows to and from the endpoints in the namespace. 

![bookinfo-allow](images/bookinfo-allow.png)
