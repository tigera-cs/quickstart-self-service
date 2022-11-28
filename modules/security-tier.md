# The Security Tier

The `security` tier will be used to implement high-level guardrails for the cluster. A `threatfeed` security policy will be enforced for all cluster workloads. The policy will `deny` egress connectivity to malicious IPs in the `threatfeed`. Tenant isolation is achieved by enforcing `tenant-1-restrict` and `tenant-2-restrict` security policies. These policies will ensure that the tenant workloads are isolated from the rest of the cluster workloads. 

> Security Policies in the `security tier`

![security-tier](images/security-tier.png)

## `threatfeed` Security Policy

The `threatfeed` security policy will have a rule that denies egress connectivity to malicious external IPs which are dynamically updated from a threatfeed. The security policy will be a [globalnetworkpolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy) that applies to all cluster workloads/pods. 

> threatfeed security policy

![threatfeed](images/threatfeed.png)

## `tenant-1-restrict` and `tenant-2-restrict` Security Policies
 
The `tenant-1-restrict` and `tenant-2-restrict` security policies will have ingress and egress rules required to isolate workloads in those tenants from the rest of the cluster workloads. Rules with the `pass` action will be used to defer security policy evaluation to subsequent tiers that match tenant-1 and tenant-2 workloads for flows that are deemed acceptable. All other ingress and egress flows will be explicitly denied using ingress and egress rules with the `deny` action. Note that the `tenant-1-restrict` and `tenant-2-restrict` policies **do not** `allow` traffic flows. The rules with the `pass` action enforce a high-level control for isolating those workloads from the rest of the cluster workloads; however, the specific traffic flows must be permitted by `allow` rules in security policies that match those workloads in subsequent tiers.  The `tenant-1-restrict` and `tenant-2-restrict` security policies will be [globalnetworkpolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy) with `NamespaceSelectors` that match tenant-01 and tenant-02 namespaces. 

> `tenant-1-restrict` security policy

![tenant-1-restrict](images/tenant-1-restrict.png)
![tenant-1-pass](images/tenant-1-pass.png)

> `tenant-2-restrict` security policy

![tenant-2-restrict](images/tenant-2-restrict.png)
![tenant-2-pass](images/tenant-2-pass.png)


## `security-default-pass` Security Policy

The `security-default-pass` security policy will have the lowest precedence in the security tier. It is deployed to ensure that traffic flows for all other workloads (except tenant-01 and tenant-02 workloads) will have a `pass` action so that Calico will evaluate subsequent tiers for those workloads for all ingress and egress traffic flows. It is required since the `threatfeed` security policy matched all cluster workloads. Note that if a workload is matched by a security policy in a tier, any traffic flow that **does not** match an `allow` rule for that workload either in that security policy or a subsequent security policy that matches the workloads in the **same tier**, will have an implicit `deny` behavior. This can be circumvented by deploying a security policy that matches the workload and has `pass` rules for all ingress and egress traffic flows. The `security-default-pass` security policy will be a [globalnetworkpolicy](https://docs.tigera.io/reference/resources/globalnetworkpolicy) that applies to all cluster workloads/pods.    

> security-default-pass security policy

![security-default-pass](images/security-default-pass.png)

#### <div align="right">  [Next: Lesson 3 - The Platform Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/platform-tier.md) </div>

