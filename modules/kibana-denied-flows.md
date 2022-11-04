
# Using Kibana to Identify Denied Flows

The `Tigera Secure EE Flow Logs` dashboard can be used to filter denied flow logs in Kibana. The flow filtering options can be used to narrow down specifi flows. 

![kibana-block-flows](images/kibana-block-flows.gif)

## Denied flows from `monitoring-pod`

### `monitoring` to `hipstershop`

![kibana-m-f](images/kibana-m-f.png)

### `monitoring` to `yaobank`

![kibana-m-c](images/kibana-m-c.png)

### `monitoring` to `bookfino`

![kibana-m-p](images/kibana-m-p.png)


## Denied flows from `loadgeneratorv2`

![kibana-l-f](images/kibana-l-f.png)

## Denied flows from `ratings`

![kibana-r-g](images/kibana-r-g.png)

#### <div align="right">  [Click Next -> Lesson 19 - Remediate Security Policies to Permit Denied Flows](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/remediate-security-policies.md) </div>