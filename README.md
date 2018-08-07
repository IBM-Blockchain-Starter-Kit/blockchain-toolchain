# Blockchain Toolchain Automation

The toolchains contained in this repository will configure your development environment with version tracking (cloning from a scaffolding repo) and continuous integration (using our build-test-deploy framework) on the bluemix domain. 

## Prerequisites

You will need an [IBM Cloud account](https://console.bluemix.net/dashboard/apps/) with permissions to create new services on the bluemix domain. 

You will need a [IBM Blockchain platform](https://console.bluemix.net/docs/services/blockchain/index.html#ibm-blockchain-platform) payment plan associated with this account. A starter plan or enterprise plan will work. 

## How it works

Upon clicking one of the [buttons](#choose-your-desired-platform) below, you will be redirected to a [bluemix toolchain](https://console.bluemix.net/docs/services/ContinuousDelivery/toolchains_about.html) creation page. In order for this to work properly, you should be logged into your bluemix account. On this page, you will be prompted with a toolchain creation form. 

### Toolchain Setup

The top section of the form configures the name of the toolchain service, the region where the service will be hosted, and the cloud foundry organization which will administrate the service's settings. You should edit these fields as desired.

![Toolchain Config Image](assets/toolchain_config.png)

The rest of the form will be specifically tailored to the layer of the stack you are working on, and what Hyperledger framework you have selected. More information is available on the following layer specific walkthroughs. 

Smart Contract Toolchain Walkthrough: [here](https://github.com/IBM-Blockchain-Starter-Kit/blockchain-toolchain/blob/chaincode/README.md)

API Toolchain Walkthrough: [here](https://github.com/IBM-Blockchain-Starter-Kit/blockchain-toolchain/blob/api/README.md)

UI Toolchain Walkthrough: *coming soon...*

## Choose a Framework and Layer

One-Click Toolchain Creation|Layer|Framework|Language
---|---|---|---
[![Deploy To Bluemix](https://console.ng.bluemix.net/devops/graphics/create_toolchain_button.png)](https://console.ng.bluemix.net/devops/setup/deploy/?repository=https://github.com/IBM-Blockchain-Starter-Kit/blockchain-toolchain&branch=chaincode&platform=go&bootstrapRepo=https://github.com/IBM-Blockchain-Starter-Kit/chaincode-bootstrap.git)| Smart Contract | Fabric | GoLang
*Coming Soon...* | API | Fabric | Express


You can also create a toolchain using the following API to inject an existing repository as the input for the delivery pipeline. 

```
https://console.ng.bluemix.net/devops/setup/deploy/
?repository=https://github.com/IBM-Blockchain-Starter-Kit/blockchain-toolchain
&branch=chaincode
&platform=<your_platform>
&bootstrapRepo=<your_source_repo_url_here>
```

This is only currently available for the chaincode layer. Valid platforms are 'go', 'composer', and 'js'. 

