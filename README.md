# ESCluster
This Templates helps to create AWS ElasticSearch service cluster. 
The following parameters can be configured as the part of creating the stack 
1. Domain Name 
      Name for the ElasticSearch Domain.
2. Environment Name 
      To define environment - QA / PROD. 
3. ElasticSearchVersion 
      The desired version of elasticsearch . AWS provides the following versions { 6.0, 5.5, 5.3, 5.1, 2.3 ,1.5 }.
4. IngressAllow 
     This will help to proide IP based restrictions on ES API calls. Its recommended to allow access only from your data source . 
5. KibanaAllow 
     This parameter helps to allow to which IP address the Kibana access should be allowed.  
     Depending on usage you may allow access only from desired network or wide open to internet. 
6. InstanceType 
     Select what type of EC2 instance to be used with the elasticsearch nodes. 
7. InstanceCount 
     Define how many nodes must to be present on the cluster. 
8. StorageSize
     Define the size of storage required. Recommented minimum is 20GB
9. StorageType 
     Define the type of storage volume. magnetic = standard and ssd = gp2. 

Use Cases Tested
1. Have been verfied with 3 regions. 
2. Stack update can be used to increase / decrease the number of nodes in the cluster. 
3. Stack update can be used to change the underlyting instance type on the cluster. 
4. Stack can be udpate to increase the storage size. 

In all 4 cases domain name should not be modified since it goes for exising cluster udpate. 

Notes:
Kibana URL of Elastic Search endpoint can be accessed over the Cloudformation Outputs. 
