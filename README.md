# IBM Cloud Cluster

In this tutorial , we will guide you thru step by step how to provision a Kubernetes Cluster for yourself. You need to have an IBM Cloud account, which you can create [here]

## Provisioning a Kubernetes cluster on IBM Cloud

* Click the **Catalog** button on the top 
* Select **Service** from the catalog
* Search for **Kubernetes Service** and click on it
![Kubernetes](/kubernetes-select.png)
* You are now at the Kubernetes deployment page ,you need to specify some details about the cluster 
* Choose a plan **standard** or **free** , the free plan only has one worker node and no subnet , to provision a standard cluster , you will need to upgrade you account to Pay-As-You-Go 
  *To upgrade to a Pay-As-You-Go account, complete the following steps:

  * In the console, go to Manage > Account.
  * Select Account settings, and click Add credit card.
  * Enter your payment information, click Next, and submit your information
* Choose **classic** or **VPC** , read the [docs] and choose the most suitable type for yourself 
 ![VPC](/infra-select.png)
* Now choose your location settings , for more information please visit [Locations]
  * Choose **Geography** (continent)
![continent](/location-geo.png)
  * Choose **Single** or **Multizone** , in single zone your data is only kept in on datacenter , on the other hand with Multizone it is distributed to multiple zones , thus  safer in an unforseen zone failure 
![avail](/location-avail.png)
  * Choose a **Worker Zone** if using Single zones or **Metro** if Multizone
 ![worker](/location-worker.png) 
    * If you wish to use Multizone please set up your account with [VRF] or [enable Vlan spanning]
    * If at your current location selection , there is no available Virtual LAN , a new Vlan will be created for you 
 
* Choose a **Worker node setup** or use the preselected one , set **Worker node amount per zone**
![worker-pool](/worker-pool.png)
* Choose **Master Service Endpoint** ,  In VRF-enabled accounts, you can choose private-only to make your master accessible on the private network or via VPN tunnel. Choose public-only to make your master publicly accessible. When you have a VRF-enabled account, your cluster is set up by default to use both private and public endpoints. For more information visit [endpoints].
![endpoints](/endpoints.png)
* Give cluster a **name**

![name-new](/name-new.png)
* Give desired **tags** to your cluster , for more information visit [tags]

![tags-new](/tasg-new.png)
* Click **create**
![create-new](/create-new.png)

* Wait for you cluster to be provisioned 
![cluster-prepare](/cluster-prepare.png)
* Your cluster is ready for usage 

![cluster-ready](/cluster-done.png)

[here]: <http://cloud.ibm.com/registration>
