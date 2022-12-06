# Service Graph and Flow Visualization - Analysing Application Flows

## Analyze Traffic to and from a Namespace

Navigate to the global view of the Service Graph and click on a namespace. The right pane will provide a summarized view of the traffic flows in and out of the namespace. 

> Service Graph - Global View

![SG Application Flows](images/sg-hipstershop.png)

> Traffic Summary for the `hipstershop` namespace

![SG Application Flows](images/sg-app-flow.png)

## Analyze Traffic to and from a Deployment

Navigate to the `hipstershop` namespace and click on the `frontend` deployment. The right pane will provide a summarized view of the traffic flows in and out of the deployment. 

> Service Graph - Namespace View

![SG Application Flows](images/sg-frontend.png)

> Traffic Summary for the `frontend` deployment

![SG Application Flows](images/sg-frontend-summary.png)

## Using the Flow Visualization to Analyze Flows for a Deployment

Flow Visualization provides the ability to filter flows per namespace and deployment. Select a namespace and deployment to retrieve a list of summarized flows. 

> Traffic Summary for the `frontend` deployment in Flow Visualization

![SG Application Flows](images/fv-frontend.png)

Click on a flow to retrieve detailed information on security policy evaluation, source and destination labels, and traffic summary. 

> Detailed flow information

![SG Application Flows](images/fv-frontend-detailed.png)

---
## Lesson Video

[![Analyze Application Flows](images/sgfvaa.png)](https://tigera.wistia.com/medias/hitppj9mjk)

#### <div align="right">  [Click Next -> Lesson 4 - Anayze Flows to kube-dns](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/analyze-kube-dns.md) </div>