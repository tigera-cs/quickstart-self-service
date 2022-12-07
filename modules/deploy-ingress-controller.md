# Deploy Ingress Controller

> ### Quick Access - [Lesson Lab Tasks](#Lesson-Lab-Tasks) 

In this lesson an ingress controller will be deployed to the cluster. An ingress controller will faciliate the creation of ingress resources to access the applications deployed in the previous lesson. In the ingress will be deployed using the below manifest; however, you can deploy an ingress controller of your choosing. 

```yaml
https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.4.0/deploy/static/provider/cloud/deploy.yaml
```

Validate the ingress pods and services one successfully deployed. 

```bash
tigera@amp ~ % kubectl get all -n ingress-nginx
NAME                                           READY   STATUS      RESTARTS   AGE
pod/ingress-nginx-admission-create-plw7z       0/1     Completed   0          28d
pod/ingress-nginx-admission-patch-np85b        0/1     Completed   1          28d
pod/ingress-nginx-controller-5cc4f7674-8mfbm   1/1     Running     0          28d

NAME                                         TYPE           CLUSTER-IP     EXTERNAL-IP     PORT(S)                      AGE
service/ingress-nginx-controller             LoadBalancer   10.0.122.1     20.221.88.154   80:30339/TCP,443:30156/TCP   28d
service/ingress-nginx-controller-admission   ClusterIP      10.0.147.115   <none>          443/TCP                      28d

NAME                                       READY   UP-TO-DATE   AVAIlabel   AGE
deployment.apps/ingress-nginx-controller   1/1     1            1           28d

NAME                                                 DESIRED   CURRENT   READY   AGE
replicaset.apps/ingress-nginx-controller-5cc4f7674   1         1         1       28d

NAME                                       COMPLETIONS   DURATION   AGE
job.batch/ingress-nginx-admission-create   1/1           8s         28d
job.batch/ingress-nginx-admission-patch    1/1           8s         28d
```

# Lesson Lab Tasks

### Deploy the ingress controller and validate resources

```yaml
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.4.0/deploy/static/provider/cloud/deploy.yaml
kubectl get all -n ingress-nginx
```

# Lesson Video

#### <div align="right">  [Click Next -> Lesson 4 - Create Ingress Resources for Applications](https://github.com/tigera-cs/quickstart-self-service/blob/main/modules/create-ingress-resources.md) </div>