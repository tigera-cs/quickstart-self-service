# Validate Security Policies

## `tenant-1-pass-all` Security Policy


### Evaluate `Pass: Any Protocol` Ingress and Egress Rule Metrics

![evaluate-tenant-1-pass-all-gif](images/evaluate-tenant-1-pass-all.png)

### Evaluate Kibana Flow Logs for `Pass: Any Protocol` Ingress Rule

> `reporter: "dst" and policies:{all_policies:*tenant-1-pass-all|pass|2*}`

![kibana-dst-tenant-1-pass-all](images/kibana-dst-tenant-1-pass-all.png)

### Evaluate Kibana Flow Logs for `Pass: Any Protocol` Egress Rule

> `reporter: "src" and policies:{all_policies:*tenant-1-pass-all|pass|3*}`

![kibana-src-tenant-1-pass-all](images/kibana-src-tenant-1-pass-all.png)


## `tenant-2-pass-all` Security Policy

### Evaluate `Pass: Any Protocol` Ingress and Egress Rule Metrics

![evaluate-tenant-2-pass-all-gif](images/evaluate-tenant-2-pass-all.png)

### Evaluate Kibana Flow Logs for `Pass: Any Protocol` Ingress Rule

### Evaluate Kibana Flow Logs for `Pass: Any Protocol` Egress Rule

> `reporter: "src" and policies:{all_policies:*tenant-2-pass-all|pass|2*}`

![kibana-src-tenant-2-pass-all](images/kibana-src-tenant-2-pass-all.png)


## `tenant-1-default-allow` Security Policy

![evaluate-tenant-1-default-allow.png](images/evaluate-tenant-1-default-allow.png)

### Evaluate Kibana Flow Logs for `tenant-2-default-allow` Security Policy

> `policies:{all_policies:*tenant-1-default-allow*}`

![kibana-tenant-1-default-allow.png](images/kibana-tenant-1-default-allow.png)


## `tenant-2-default-allow` Security Policy

![evaluate-tenant-2-default-allow.png](images/evaluate-tenant-2-default-allow.png)

### Evaluate Kibana Flow Logs for `tenant-2-default-allow` Security Policy

> `policies:{all_policies:*tenant-2-default-allow*}`

![kibana-tenant-2-default-allow.png](images/kibana-tenant-2-default-allow.png)