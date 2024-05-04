# Introduction to LoadBalancer Service
*A Load Balancer is a service type that provides external access to a set of pods in a cluster. It distributes incoming traffic among the pods to ensure high availability, scalability, and reliability of the application running in the cluster.*

Load balancing becomes necessary in various scenarios, primarily when you have multiple instances of your application running simultaneously, and you want to distribute incoming traffic among them efficiently.

<image src="./images/LB-01.png" width="800">

In above scenario,you needs to deploy a separate Load Balancer VM in your environment to providing a single URL for users to access the application. This Load Balancer will be responsible for forwarding requests from users to any of the nodes hosting the application.


## Creating a Load-Balance Service in Kubernetes

To create a Loadbalance-service you need to flow this steps:

1.  **Creating a Definition file**:To create a Loadbalance-service definition file you simply need to modify the 'type' as LoadBalance in spec field,the remaining portion will be same as other services you have created before.

<image src="./images/LB-02.png" width="400">

2. **Run kubectl Create Command**: Once you've created the definition file, apply it to your Kubernetes cluster using the following command:
   
    ```bash
    kubectl apply -f load-balancer-service.yaml
    ```
3. **Check Deployment Status**: After applying the deployment, verify its status using the following command:

    ```bash
    kubectl get services
    ```
