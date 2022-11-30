# The Appsec Tier

The `appsec` tier implements fine-grained security policies that use policy label selectors to match specified endpoints/deployments in the namespace.

> Security Policies in the `appsec tier`

![appsec-tier](images/appsec-tier.png)

## `deployment(hipstershop)` Security Policies

The `appsec` tier implements a security policy for each deployment in the `hipstershop` namespace. Each security policy will have granular ingress and egress rules permitting traffic flows to and from each deployment. Unlike policies in the `application` tier, workloads matched in the `appsec` tier require defining policies to ensure that workloads in the same namespace can communicate.

![appsec-policies](images/appsec-policies.png)

## Implicit Deny

Similar to the `application` tier, the `appsec` tier will also have an implicit deny for traffic flows not explicitly permitted for endpoints matched/selected by security policies in the `tier`. Note that although the implicit deny is logically represented at the bottom of the tier, the behavior is enforced by the last security policy in the `tier` that matches a particular endpoint. 

#### <div align="right">  [Next: Lesson 6 - The Default Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/default-tier.md) </div>