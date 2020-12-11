# Cloud Adoption USing Microsoft Azure 

The cloud adoption and microsoft Azure 

## Installing and Using Kibana 

Cloud adoption is growing, it has become more important than ever to monitor your cloud resources, 
activities in your cloud accounts and track the events happening within your services.

Azure tracks all the events in your Azure Account/Subscription and publishes it to Azure Activity 
Log service. As the number of events grow it becomes really difficult to filter these logs and translate them into readable information.

##Installation process

Kibana can be deployed in addition to Elasticsearch, providing a visual window and UI into the data within Elasticsearch. The version of Kibana deployed is always 
the same as the version of Elasticsearch, ensuring compatibility between the products.

```
Examples 
```

## Installtion
The Azure VM SKU to use for Kibana. Different VM SKUs have different CPU, RAM, temporary storage space and network bandwidth. 
The Kibana VM always uses standard storage for the OS disk. The default value is Standard_A2_v2.

 
## vmKibanaAcceleratedNetworking
    Whether to enable accelerated networking for Kibana, which enables single root I/O virtualization (SR-IOV) to a VM, greatly improving its networking performance. Valid values are Default, Yes, No. The default is Default, which enables accelerated networking for the VM SKUs known to support it. 

    It is recommended that you run your additional yaml through a linter before starting a deployment, as incorrectly formatted yaml will fail the deployment.

##Kibana is deployed with

    a public IP address, whose fully qualified domain name and IP address can be retrieved from the deployment outputs
    a network security group that allows TCP traffic from the internet on port 5601, to allow browsers to interact with Kibana. Port 22 also allows TCP traffic from the internet, to allow a user to connect using SSH, and use Kibana as a jumpbox to connect to Elasticsearch node VMs.

## Kibana communicates with Elasticsearch through the internal load balancer
