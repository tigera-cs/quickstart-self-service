# Flow Log Aggregation
> ### Quick Access - [Lesson Lab Tasks](#Lesson-Lab-Tasks) 

Calico Enterprise enables flow log aggregation for pod/workload endpoints by default and uses an aggressive aggregation level to reduce log volume. The level assumes that most users do not need to see pod IP information (due to the ephemeral nature of pod IP address allocation). However, pod or destination IP information can sometimes be helpful when analyzing traffic flows.

The table below summarizes the aggregation levels. 
>  - Aggregation 0 - no aggregation
>  - Aggregation 1 - source port
>  - Aggregation 2 - source port, source IP, destination IP, source pod prefix, and destination pod prefix


![flow-log-aggregation](images/flow-log-aggregation.png)

# Lesson Lab Tasks

### Apply a log aggregation of 1 for Allowed and Denied Traffic

```bash
kubectl patch felixconfiguration.p default -p '{"spec":{"flowLogsFileAggregationKindForAllowed":1}}'
kubectl patch felixconfiguration.p default -p '{"spec":{"flowLogsFileAggregationKindForDenied":1}}'
```

# Lesson Video


<p align="center">
  
[![video-flow-log-aggregation](images/vfla.png)](https://tigera.wistia.com/medias/yhitu7fhop)

</p>

---

#### <div align="right">  [Click Next -> Lesson 3 - Service Graph and Flow Visualization - Analyzing Application Flows](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/analyze-service-graph.md)</div>