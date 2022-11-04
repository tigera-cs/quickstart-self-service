# The Default Tier

![default-tier](images/default-tier.png)

## `tenant-01-default-deny` Security Policy

The `tenant-01-default-deny` security policy will have rules to deny all ingress and egress traffic flows to and from tenant-1 workloads. The security policy is the final gatekeeper for endpoints in the `hipstershop` and `yaobank` namespaces and will ensure that only traffic flows allowed by security policy rules in preceding tiers are accepted. Having a separate default-deny security policy for tenant-01 workloads enables the implementation of zero-trust micro-segmentation for those workloads irrespective of other worklooads in the cluster. The `tenant-1-default-deny` security policy will be [globalnetworkpolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy) that matches the tenant-01 namespaces.

## `tenant-02-default-deny` Security Policy


The `tenant-02-default-deny` security policy will have rules to deny all ingress and egress traffic flows to and from tenant-2 workloads. The security policy is the final gatekeeper for endpoints in the `bookfinfo` namespace and will ensure that only traffic flows allowed by security policy rules in preceding tiers are accepted. Similar to tenant-01, having a separate default-deny security policy for tenant-02 workloads enables the implementation of zero-trust micro-segmentation for those workloads irrespective of other worklooads in the cluster. The `tenant-2-default-deny` security policy will be [globalnetworkpolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy) that matches the tenant-01 namespaces.

#### <div align="right">  [Click Next -> Module 4 - Methodology for Implementing Zero-Trust Microsegmentation](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/module-4-introduction.md) </div>