# The Default Tier

![default-tier](images/default-tier.png)

## `tenant-01-default-deny` Security Policy

The `tenant-01-default-deny` security policy will have rules to deny all ingress and egress traffic flows to and from tenant-1 workloads. The security policy is the final gatekeeper for endpoints in the `hipstershop` and `yaobank` namespaces and will ensure that only traffic flows allowed by security policy rules in preceding tiers are accepted. Having a separate default-deny security policy for tenant-01 workloads enables the implementation of zero-trust micro-segmentation for those workloads irrespective of other worklooads in the cluster. 

## `tenant-02-default-deny` Security Policy


The `tenant-02-default-deny` security policy will have rules to deny all ingress and egress traffic flows to and from tenant-2 workloads. The security policy is the final gatekeeper for endpoints in the `bookfinfo` namespace and will ensure that only traffic flows allowed by security policy rules in preceding tiers are accepted. Similar to tenant-01, having a separate default-deny security policy for tenant-02 workloads enables the implementation of zero-trust micro-segmentation for those workloads irrespective of other worklooads in the cluster. 

