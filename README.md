# Quickstart Self-paced Workshop (WIP)

<img src="/modules/images/Calico_Cloud_logo_badge.svg" width="300" height="300">

Supporting documentation for the Calico Cloud Quickstart Self Guided Workshop. The objective of this workshop is to help participants understand security policy frameworks and methodologies to implement identity-based microsegmentation in Kubernetes. 

### **Introduction**

[![intro](/modules/images/intro.png)](https://tigera.wistia.com/medias/qwgycmgsfe)

## Table of Contents

### **01. Module 1  - Lab Setup**

   - [Module 1 - Introduction](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/module-1-introduction.md)
   - [Lesson 1 - Connect Cluster to Calico Cloud](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/connect-cluster-to-calico-cloud.md)
   - [Lesson 2 - Deploy Applications](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/deploy-applications.md)
   - [Lesson 3 - Deploy Ingress Controller](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/deploy-ingress-controller.md)
   - [Lesson 4 - Create Ingress Resources for Applications](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/create-ingress-resources.md)
     
### **02. Module 2 - Calico Security Policy Constructs**

   - [Module 2 - Introduction](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/module-2-introduction.md)
   - [Lesson 1 - The Anatomy of a Security Policy](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/policies-rules.md) 
   

### **03. Module 3 - Security Policy Framework for Identity-Based Micro-segmentation**

   - [Module 3 - Introduction](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/module-3-introduction.md)
   - [Lesson 1 - Security Policy Framework Overview](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policy-framework-overview.md)
   - [Lesson 2 - The Security Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-tier.md)
   - [Lesson 3 - The Platform Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/platform-tier.md)
   - [Lesson 4 - The Application Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/application-tier.md)
   - [Lesson 5 - The Appsec Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/appsec-tier.md)
   - [Lesson 6 - The Default Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/default-tier.md)
     
### **04. Module 4 - Methodology for Implementing Zero-Trust Microsegmentation**

- [Module 4 - Introduction](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/module-4-introduction.md)

####   **1. Step 1 - Identify**
   
   - [Lesson 1 - Service Graph - Views and Layers](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/views-and-layers-sg.md)

####  **2. Step 2 - Analyze**
   - [Lesson 2 - Flow Log Aggregtion](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/log-aggregation.md)
   - [Lesson 3 - Service Graph and Flow Visualization - Analyzing Application Flows](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/analyze-service-graph.md)
   - [Lesson 4 - Anaylze Flows to kube-dns](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/analyze-kube-dns.md) 
   - [Lesson 5 - Analyze Traffic to External Services using Service Graph and Kibana](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/analyze-external-services.md)
   - [Lesson 6 - Create Domain Networksets for External Services](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/analyze-networksets-external-services.md)

####   **3. Step 3 - Deploy Security Policies for Applications**
   - [Lesson 7 - Deploy Tiers](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/deploy-tiers.md)
   - [Lesson 8 - Security Policies in the Default Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policies-default-tier.md)
   - [Lesson 9 - Security Policies in the Security Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policy-in-security-tier.md)
   - [Lesson 10 - Security Policies in the Platform Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policy-in-platform-tier.md)
   - [Lesson 11 - Security Policies in the Application Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policies-in-application-tier.md)
   - [Lesson 12 - Security Policies in the Appsec Tier](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/security-policies-in-appsec-tier.md)
   - [Lesson 13 - Validate Security Policies](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/validate-security-policies.md)

####  **4. Step 4 - Enforce Default Deny for Applications**
   - [Lesson - 14 - Enforce Default Deny for Application Namespaces](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/enforce-default-deny.md)


####  **5. Step 5 - Assess and Remediate**
   - [Lesson 15 - Introduce New Flows](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/new-flows.md)
   - [Lesson 16 - Using Service Graph to Identify Denied Flows](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/sg-denied-flow.md)
   - [Lesson 17 - Using Flow Vizualization to Identify Denied Flows](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/fv-denied-flows.md)
   - [Lesson 18 - Using Kibana to Identify Denied Flows](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/kibana-denied-flows.md)
   - [Lesson 19 - Remediate Security Policies to Permit Denied Flows](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/remediate-security-policies.md)
   - [Lesson 20 - Validate Remediated Security Policies](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/validate-remediate-security-policies.md)

### **05. Module 5 - Expanding the Security Policy Framework**

[Coming Soon]

---
## Quick Access - Lesson Videos

- [1.1 - Connect Cluster to Calico Cloud](https://tigera.wistia.com/medias/zs6oc6j1uj)
- [1.2 - Deploy Applications](https://tigera.wistia.com/medias/dsa4gj6vox)
- [4.1 - Service Graph - Views and Layers](https://tigera.wistia.com/medias/if9ccnwrdp)
- [4.2 - Flow Log Aggregation](https://tigera.wistia.com/medias/yhitu7fhop)
- [4.3 - Service Graph and Flow Visualization - Analyzing Application Flows](https://tigera.wistia.com/medias/hitppj9mjk)
- [4.7 - Deploying Security Policy Tiers](https://tigera.wistia.com/medias/9qdjr5onoj)
- [4.12 - Service Graph - Security Policy Processing Sequence](https://tigera.wistia.com/medias/lymcn38m3b)
- [4.14 -  Enforce Default Deny for Application Namespaces](https://tigera.wistia.com/medias/nyvmnpsbu1)
- [4.16 - Using Service Graph to Identify Denied Flows](https://tigera.wistia.com/medias/88j386d49p)
- [4.17 - Using Flow Vizualization to Identify Denied Flows](https://tigera.wistia.com/medias/k5en6cvfob)

## Security Policy Templates

   - [Policy Tiers](https://github.com/tigera-cs/quickstart-self-service/blob/main/manifests/securitypolicies/tiers.yaml)

---
## Upcoming Lessons

- source and destination reporting
- kibana filtering based on index
- Using services in security policy rules 
- Security policy evaluation in logs

