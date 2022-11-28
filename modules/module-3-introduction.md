
# Module 3 - Introduction

## Security Domains

In this module, you will explore a security policy framework to secure tenants and applications. Calico offers a powerful policy model to implement a hierarchical approach to security. Unlike traditional firewalls, which implement security as traffic transits specific points in the network, Calico enforces security for each endpoint or workload in the cluster. Understanding the concept of `security domains` is essential to implement hierarchical controls for Kubernetes workloads. A security policy framework that leverages Calico's `tiers` and `policy constructs` can be developed once a cluster's `security domains` are identified. 

The lab cluster comprises the following `security domains`

1.  **The cluster** - The cluster can be considered a `security domain`. For example, consider enforcing a `threatfeed` security policy denying egress connectivity to malicious IPs for all cluster workloads.

2.  **Tenants** - Tenants are separate `security domains`. For example, isolating `tenant-1` and `tenant-2` workloads from other cluster workloads. The concept of tenancy can be extended to other forms of isolation. For instance, restricting PCI workloads from other cluster endpoints. It is a collection of applications or namespaces for which a specific security declaration is enforced. 

3.  **Namespaces** - A namespace is a Kubernetes construct used to isolate groups of resources such as deployments, services, and ConfigMaps, among others. Microservices that make up an application are typically organized into a single namespace and can be treated as separate `security domains`. For example, consider protecting an application from other applications in the cluster or the same tenant. 

4.  **Endpoint Groups** - A microservice comprises endpoint groups such as `deployments`, `statefulsets`, and `daemonsets`. Microservices, even in the same namespace, must be protected from each other to limit the blast radius if one is compromised. For example, consider a `frontend` and a `backend` microservice in the same namespace; they are in separate `security domains` and must be protected by security policies.   

> Security domains

![Security Domains](images/security-domains.png)

> #### <div align="right">  [Next: Lesson 1 - Security Policy Framework Overview](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policy-framework-overview.md) </div>


