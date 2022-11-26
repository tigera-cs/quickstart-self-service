
# Module 3 - Introduction

## Security Domains

In this module, you will explore a security policy framework to secure tenants and applications. Calico offers a powerful policy model to implement a hierarchical approach to security. Unlike traditional firewalls, which implement security as traffic transits specific points in the network, Calico enforces security for each endpoint or workload in the cluster. Understanding the concept of `security domains` is essential to implement hierarchical controls for Kubernetes workloads. A security policy framework that leverages Calico's `tiers` and `policy constructs` can be developed once the `security domains` of a cluster are identified. 

The lab cluster comprises the following `security domains`

1.  **The cluster** - The cluster can be considered a `security domain`. For example, consider enforcing a `threatfeed` security policy denying egress connectivity to malicious IPs for all cluster workloads.

2.  **Tenants** - Tenants are separate `security domains`. For example, isolating `tenant-1` and `tenant-2` workloads from other cluster workloads. The concept of tenancy can be extended to other forms of isolation. For instance, restricting PCI workloads from other cluster endpoints. It is a collection of applications or namespaces for which a specific security declaration is enforced. 

3.  **Namespaces** - Namespaces are a logical Kubernetes construct and can be used to organize Kubernetes resources such as deployments and services. A namespace would typically consist of a collection of microservices that make up an application. Namespaces can also be considered separate `security domains`. For example, applications must be protected from other applications within the same tenant.

4.  **Deployments** - Deployments are a Kubernetes construct comprising workloads or pods that make up microservices. Microservices must be protected from other microservices to limit the blast radius if a microservice were to get compromised. For example, a `frontend` microservices and a `backend` microservice can be in the same namespace but can still be considered separate `security domains` as the function and criticality of the microservices differ and must be protected by separate security policies.   

> Security domains

![Security Domains](images/security-domains.png)

> #### <div align="right">  [Next: Lesson 1 - Security Policy Framework Overview](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policy-framework-overview.md) </div>


