
# Using Kibana to Identify Denied Flows

The `Tigera Secure EE Flow Logs` dashboard can be used to filter denied flow logs in Kibana. 

![kibana-block-flows](images/kibana-block-flows.gif)

## Denied flow from `monitoring-pod`

### `monitoring` to `hipstershop`

![kibana-m-f](images/kibana-m-f.png)

### `monitoring` to `yaobank`

![kibana-m-c](images/kibana-m-c.png)

### `monitoring` to `bookfino`

![kibana-m-p](images/kibana-m-p.png)


## Denied flow from `loadgeneratorv2`

![kibana-l-f](images/kibana-l-f.png)

## Denied flow from `ratings`

![kibana-r-g](images/kibana-r-g.png)