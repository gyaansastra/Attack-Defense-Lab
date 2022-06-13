# Multi Tier VNet with NSGs and Bastian

![Azure Public Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.network/nsg-dmz-in-vnet/PublicLastTestDate.svg)
![Azure Public Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.network/nsg-dmz-in-vnet/PublicDeployment.svg)
![Best Practice Check](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.network/nsg-dmz-in-vnet/BestPracticeResult.svg)

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https://raw.githubusercontent.com/gyaansastra/Attack-Defence-Lab/main/armtemplates/vnet/template.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https://raw.githubusercontent.com/gyaansastra/Attack-Defence-Lab/main/armtemplates/vnet/template.json)

This template creates a VNet with 4 subnets:

* **NetOps** - _NetOps_Subnet / 172.16.1.0/24_
* **Incubator** - _Incubator_Subnet / 172.16.2.0/24_
* **SecOps** - _SecOps_Subnet / 172.16.3.0/24_
* **OffSec** - _OffSec_Subnet / 172.16.4.0/24_

It also creates three Network Security Groups - one per subnet:

* **NetOps** - _NetOps_Subnet_Nsg_
* **Incubator** - _Incubator_Subnet_Nsg_
* **SecOps** - _SecOps_Subnet_Nsg_
* **OffSec** - _OffSec_Subnet_Nsg_

Each NSG is then associated with a subnet:

* _NetOps_Subnet_ to _NetOps_Subnet_Nsg_
* _Incubator_Subnet_ to _Incubator_Subnet_Nsg_
* _SecOps_Subnet_ to _SecOps_Subnet_Nsg_
* _OffSec_Subnet_ to _OffSec_Subnet_Nsg_

VNet is configured with Bastian:

* _Bastion_ to _Bastion_PubIP_