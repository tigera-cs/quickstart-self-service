# Create Domain Networsets for External Services

> ### Quick Access - [Lesson Lab Tasks](#Lesson-Lab-Tasks) 

## `ubuntu` Networkset

> `ubuntu` Networkset UI View

![ubuntu](images/ns-ubuntu.png)

> `ubuntu` Networkset manifest

```yaml
kind: GlobalNetworkSet
apiVersion: projectcalico.org/v3
metadata:
  name: ubuntu
  labels:
    ubuntu: 'true'
spec:
  nets: []
  allowedEgressDomains:
    - '*.ubuntu.com'
```

## `bloomberg` Networkset

> `bloomberg` Networkset UI View

![bloomberg](images/ns-bloomberg.png)

> `bloomberg` Networkset manifest

```yaml
kind: GlobalNetworkSet
apiVersion: projectcalico.org/v3
metadata:
  name: bloomberg
  labels:
    bloomberg: 'true'
spec:
  nets: []
  allowedEgressDomains:
    - '*.bloomberg.com'
```

# Lesson Lab Tasks

# Lesson Video

#### <div align="right">  [Click Next -> Lesson 7 - Deploy Tiers](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/deploy-tiers.md) </div>