# Quickstart Self Service Workshop

<img src="/modules/images/Calico_Cloud_logo_badge.svg" width="300" height="300">

Supporting documentation for the Calico Cloud Quickstart Self Guided Workshop. The objective of this workshop is to help participants understand security policy frameworks and methodologies to implement zero-trust microsegmentation in Kubernetes. 

## Table of Contents

### **Introduction**


### **01. Module 1  - Lab Setup**

   - [Module 1 - Introduction](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/module-1-introduction.md)
   - [Lesson 1 - Connect Cluster to Calico Cloud](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/connect-cluster-to-calico-cloud.md)
   - [Lesson 2 - Deploy Applications](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/deploy-applications.md)
   - [Lesson 3 - Deploy Ingress Controller](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/deploy-ingress-controller.md)
   - [Lesson 4 - Create Ingress Resources for Applications](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/create-ingress-resources.md)
     
### **02. Module 2 - Calico Security Policy Constructs**

   - [Module 2 - Introduction](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/module-2-introduction.md)
   - [Lesson 1 - Security Policies, Rules and Selectors](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/policies-rules.md) 
   projectcalico.org/name
   projectcalico.org/servicenedpoint

### **03. Module 3 - Security Policy Framework for Zero-Trust Microsegmentation**

   - [Module 3 - Introduction](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/module-3-introduction.md)
   - [Lesson 1 - Security Policy Framework Overview](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/security-policy-framework-overview.md)
   - [Lesson 2 - The Security Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/security-tier.md)
   - [Lesson 3 - The Platform Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/platform-tier.md)
   - [Lesson 4 - The Application Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/application-tier.md)
   - [Lesson 5 - The Appsec Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/appsec-tier.md)
   - [Lesson 6 - The Default Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/default-tier.md)
     
### **04. Module 4 - Methodology for Implementing Zero-Trust Microsegmentation**

####   **1. Step 1 - Identify**
   
   - [Lesson 1 - Service Graph - Views and Layers](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/views-and-layers-sg.md)

####  **2. Step 2 - Analyze**
   - [Lesson 2 - Flow Log Aggregtion](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/log-aggregation.md)
   - [Lesson 3 - Service Graph and Flow Visualization - Analyzing Application Flows](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/analyze-service-graph.md)
   - [Lesson 4 - Anayze Flows to kube-dns](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/analyze-kube-dns.md) 
   - [Lesson 5 - Analyze Traffic to External Services using Service Graph and Kibana](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/analyze-external-services.md)
   - [Lesson 6 - Create Domain Networksets for External Services](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/analyze-networksets-external-services.md)

####   **3. Step 3 - Deploy Security Policies for Applications**
   - [Lesson 7 - Deploy Tiers](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/deploy-tiers.md)
   - [Lesson 8 - Security Policies in the Default Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/security-policies-default-tier.md)
   - [Lesson 9 - Security Policies in the Security Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/security-policy-in-security-tier.md)
   - [Lesson 10 - Security Policies in the Platform Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/security-policy-in-platform-tier.md)
   - [Lesson 11 - Security Policies in the Application Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/security-policies-in-application-tier.md)
   - [Lesson 12 - Security Policies in the Appsec Tier](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/security-policies-in-appsec-tier.md)

####  **4. Step 4 - Enforce Default Deny for Applications**
   - [Lesson - 13 - Enforce Default Deny for Application Namespaces](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/enforce-default-deny.md)


####  **5. Step 5 - Assess and Remediate**
   - [Lesson 14 - Using Service Graph to Identify Denied Flows](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/sg-denied-flow.md)
   - [Lesson 15 - Using Flow Vizualization to Identify Denied Flows](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/fv-denied-flows.md)
   - [Lesson 16 - Using Kibana to Identify Denied Flows](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/kibana-denied-flows.md)
   - [Lesson 17 - Remediate Security Policies to Permit Denied Flows](https://github.com/aadhilam/quickstart-self-service/blob/main/modules/remediate-security-policies.md)

### **05. Module 5 - Expanding the Security Policy Framework**

---
### Quick Access to Lesson Videos


- [Module 4 - Lesson 3 - Service Graph and Flow Visualization - Analyzing Application Flows](https://tigera.wistia.com/medias/hitppj9mjk)
- [Module 4 - Lesson 4 - Flow Log Aggregation](https://tigera.wistia.com/medias/yhitu7fhop)
- [Module 4 - Lesson 7 - Deploy Security Policy Tiers](https://tigera.wistia.com/medias/9qdjr5onoj)


Notes 
- source and destination reporting
     

