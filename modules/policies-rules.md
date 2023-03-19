# The Anatomy of a Security Policy

Calico's declarative policy language offers a high degree of flexibility in defining security intentions. 

> The Anatomy of a Security Policy

![anatomy-of-policy](images/anatomy-of-policy.png)

## `kind`

There are two types of security policies
- `NetworkPolicy` - Refer [NetworkPolicy](https://docs.tigera.io/reference/resources/networkpolicy) for more information.  
- `Globalnetworkpolicy` - Refer [GlobalNetworkPolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy) for more information. 

## `scope`

- A `NetworkPolicy` has a scope that applies to the namespace specified in the policy.  
- A `GlobalNetworkPolicy` has a scope that applies to either all namespaces or namespaces specified using the `namespaceSelector` in the security policy. 

## `selectors`

The following selectors are available:

- `namespaceSelector` - Selects the namespace(s) to which a [GlobalNetworkPolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy) applies. Select a specific namespace by name using the 'projectcalico.org/name' label. Note that the selector is only availabel for [GlobalNetworkPolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy).

- `serviceAccountSelector` - Selects the service account(s) to which a security policy applied. Select all service accounts in the cluster with a specific name using the `projectcalico.org/name` label. Availabel in both [NetworkPolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy) and [GlobalNetworkPolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy).

- `selector` -  Selects the endpoints to which a policy is applied. A selector is an expression that can be used to either match or unmatch resources based on their labels. Calico Enterprise label selectors support several operators, which can be combined into larger expressions using the boolean operators and parentheses. For more information, refer to [selector](https://docs.tigera.io/reference/resources/globalnetworkpolicy#selector)

## `ingress rules`

A security policy may have one or more `ingress` rules to allow traffic to the **selected** endpoints. The `source` field in the rule selects the endpoints from which traffic must be allowed. The `destination` field selects a subset of destinations from the endpoints selected/matched by the policy. 

## `egress rules`

One or more `egress` rules to allow traffic from the **selected** endpoints. The `source` field in the rule selects a subset of endpoints from the endpoints selected/matched by the policy. The `destination` field selects the endpoints to which traffic must be allowed. 


#### <div align="right">  [Next: Module 3 - Methodology for Implementing Zero-Trust Microsegmentation](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/module-3-introduction.md) </div>

