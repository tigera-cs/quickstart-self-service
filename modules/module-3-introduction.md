
# Introduction - Security Policy Framework for Zero-Trust Micro-segmentation

In this module, a security policy framework will be developed to secure the tenants and applications. Calico offeres a powerful policy-model that can be used to implement a hierarchical approach to security. Unlike traditional firewalls which implement security as traffic transits certain points in the network, Calico enforces security for each endpoint or workload in the cluster. It is important to understand the `security domains` for which controls are enforced when implementing security policies as a declarative policy language will be used to specific a security "intention" for a collections of workloads. 

This module will provide an in-depth explanation of how `tiers` and `security policies` can be used to develop a security policy framework to secure kubernetes clusters and minimize complexities related to policy management and operational overhead due to policy misconfigurations. 

![Security Domains](images/security-domains.png)

#### <div align="right">  [Click Next -> Lesson 1 - Security Policy Framework Overview](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policy-framework-overview.md) </div>


