
# Introduction - Security Policy Framework for Zero-Trust Micro-segmentation

In this module, a security policy framework will be developed to secure the tenants and applications. Calico offeres a powerful policy-model that can be used to implement a hierarchical approach to security. Unlike traditional firewalls which implement security as traffic transits certain points in the network, Calico enforces security for each endpoint or workload in the cluster. It is important to understand the `security domains` for which controls are enforced as a declarative policy language will be used to specific a security "intention" for a collections of workloads. 

This module will provide an in-depth explanation of how `tiers` and `security policies` can be used to develop a security policy framework to secure kubernetes clusters and minimize complexities related to policy management and operational overhead due to policy misconfigurations.

The following can be considered `security domains` for which security policies must be enforced.

01. **The cluster** - The entire cluster can be considered a single `security domain`. For example, a `threatfeed` security policy can be enforced for the cluster, that would `deny` egress connectivity to malicious IPs.

02. **Tenants** - Individual tenants can be considered separate `security domains`. For example, tenant-1 and tenant-2 workloads must be isolated from each other and the rest of the cluster workloads. Although we use the concepts of tenants is this workshop, this can be extended to include environment such as PCI workloads or business units in an organization sharing Kubernetes clusters. It is a collection of applications or namespaces for which a certain security "intention" must be enforced. 

03. **Namespaces** - Namespaces are a logical Kubernetes construct and can be used to organize Kubernetes resources such as deployments and services. A namespace would typicall consist of a collection of microservices that make up an application. Namespaces can also be considered separate `security domains`. For example, applications must be protected from other applications within the same tenant.

04. **Deployments** - Deployments are a Kubernetes construct 

> Security domains

![Security Domains](images/security-domains.png)

#### <div align="right">  [Click Next -> Lesson 1 - Security Policy Framework Overview](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policy-framework-overview.md) </div>


