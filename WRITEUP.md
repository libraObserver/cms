# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

APP SERVICE: A CMS app that is launched through an App Service has
acceptable prices, scalability, and availability. About the price, App Service is absolutely win VM in this small project since it have 3 tier base on project purpuse, and i will choose development and testing for optimse the price; provide high availability and auto-scaling, both vertical and horizontal scaling. Because of how little this software is, it doesn't require a lot of processing power. The lower compute requirements of a CMS software are therefore not expensive, even though the service plans are continuous and the customer is paying even when no one is using the service. The Azure portal's continuous deployment through GitHub workflows makes updating the CMS app a breeze.

VM: For a CMS app delivered through a VM, the pricing, scalability, and availability are also affordable. The price of VM base on instances and number of them running per hour; the scalability is autoscaling with virtual machine sclase sets, with limitatino is depend on platform image, 1000 nodes per scale set, or custom image, 600 nodes per scale set. The VM enables additional capabilities customization for the app. It also would really benefit developers who have already built a CMS app but it might not be supported through App Service but could work through the VM workflow. It also allows for more fine-tuning, so the developer can customize the VM to optimize their CMS app.

For me, The CMS app is lightweight, doesn't require a lot of compute power, and is simple to deploy through Azure, so I went with App Service. Python code is used by the CMS App, which is supported by App Service. 

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

APP Service: The expenses may quickly increase if the CMS app needs to be modified to provide greater compute capabilities, such as playing videos, manipulating images, integrating Jupyter notebooks, or doing something else that would call for more hardware. Another obstacle would undoubtedly be if the needed capability wasn't offered by Azure. Having no control over the server's underlying software may also result in serious problems that could break your app.

VM: This CMS may cost more if it gains popularity since it needs more hardware and processing power. It will take a little longer to onboard new developers because they need to understand how the VM has been configured. Additionally, the CMS might become substantially more expensive if it required additional computational power.
