# Deploy Security Policy Tiers

Security policy tiers will be used to secure workloads in the lab cluster. The tiers will be deployed according to the security policy framework discussed in previous lesson. 

Overview of the security policy tiers:

>  01. **Security Tier** - Cluster-wide blacklist security policies and security policies needed to isolate tenant-1 and tenant-2 workloads from the rest of the cluster workloads 

```yaml
apiVersion: projectcalico.org/v3
kind: Tier
metadata:
  name: security
spec:
  order: 200
```

>  02. **Platform Tier** - Security policies for platform components such as kube-dns and the ingress controller*

```yaml
apiVersion: projectcalico.org/v3
kind: Tier
metadata:
  name: platform
spec:
  order: 300
  ```

>  03. **Application Tier** - Namespaces scoped policies for the bookinfo and yaobank application 

```yaml
apiVersion: projectcalico.org/v3
kind: Tier
metadata:
  name: application
spec:
  order: 400
 ```

>  04. **Appsec Tier** - Granular namespace scoped policies for each deployment using policy label selectors

```yaml
apiVersion: projectcalico.org/v3
kind: Tier
metadata:
  name: appsec
spec:
  order: 500
```

>  05. **Default Tier** - Default-deny security policies for tenant-01 and tenant-02 workloads


> *The Policy Board with Tiers*

![policies board](images/policiesboard.png)


# Lesson Video

[![deploy tiers](images/vdspt.png)](https://tigera.wistia.com/medias/9qdjr5onoj)


#### <div align="right">  [Click Next -> Lesson 8 - Security Policies in the Default Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policies-default-tier.md) </div>