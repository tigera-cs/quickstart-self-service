# Module 2 - Introduction

## Security Policy Characteristics

Calico security policies are:
- Declarative - Offers a powerful policy language to define security intentions
- Label-based - Maps security policies to endpoints based on workload identity 
- Dynamic - Security policies are tightly coupled with workloads

> Security Policy Characteristics

![security-policy-characteristics](images/security-policy-characteristics.png)

## The Anatomy of a Security Policy

### `kind`

There are two types of security policies
- `NetworkPolicy` 
- `Globalnetworkpolicy`

### `scope`

- A `NetworkPolicy` has a scope that applies to the namespace specified in the policy. 
- A `GlobalNetworkPolicy` has a scope that applies to either all namespaces or namespaces specified using the `namespaceSelector` in the security policy

### `Selectors`

The following selectors are 




> The Anatomy of a Security Policy

![anatomy-of-policy](images/anatomy-of-policy.png)

