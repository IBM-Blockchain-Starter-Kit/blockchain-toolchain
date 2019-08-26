# Chaincode Toolchain Automation

This starter kit is intended to bootstrap your development experience building blockchain applications on top of Hyperledger. 

## Prerequisites

You will need an [IBM Cloud account](https://console.bluemix.net/dashboard/apps/) with permissions to create new services on the bluemix domain. 

You will need a [IBM Blockchain platform](https://console.bluemix.net/docs/services/blockchain/index.html#ibm-blockchain-platform) payment plan associated with this account. A starter plan or enterprise plan will work.

## How it works

Upon clicking one of the [buttons](#choose-your-desired-platform) below, you will be redirected to a [bluemix toolchain](https://console.bluemix.net/docs/services/ContinuousDelivery/toolchains_about.html) creation page. In order for this to work properly, you should be logged into your bluemix account. On this page, you will be prompted with a three-part form. 

### Toolchain Setup

The first section of the form configures the name of the toolchain service, the region where the service will be hosted, and the cloud foundry organization which will administrate the service's settings. You should edit these fields as desired.

![Toolchain Config Image](assets/toolchain_config.png)


### Version and Issue Tracking

The second section of the form is a git repo and issue tracker configuration. Depending on which platform you selected, a scaffolding repository containing platform-specific bootstrapping code is setup to be cloned into a gitlab repository with a corresponding issue tracker. You should edit these fields as desired.

![Version and Issue Tracking Config Image](assets/git_repo_issues_config.png)

### Continuous Integration Delivery Pipeline

The third section of the form is a delivery pipeline configuration. Here you can target existing service instances by specifying their identifiers or provide unregistered identifier(s) to create new instance(s). 

This delivery pipeline will queue a build stage when the gitlab repository is pushed to with new changes. A successful build stage in turn will queue the unitest stage. These tests should be defined in the git repository, where examples will be provided. A successful test stage will queue the deploy stage. The deploy configuration should be defined in the git repository, where examples will be provided. The deploy stage will target the services specified in the delivery pipeline form. 

![Pipeline Config Image](assets/pipeline_config.png)

## Choose your desired platform

|Platform|Language|One-Click Toolchain Creation||
|---------|----------|----------|----------|
| Fabric | JavaScript / TypeScript | [![Deploy To Bluemix](https://console.ng.bluemix.net/devops/graphics/create_toolchain_button.png)](https://console.ng.bluemix.net/devops/setup/deploy/?repository=https://github.com/abisarvepalli/blockchain-toolchain&branch=new-form&platform=js&bootstrapRepo=https://github.com/abisarvepalli/nodejs-chaincode-bootstrap.git&env_id=ibm:yp:u\s-south) | [TypeScript Sample Chaincode](https://github.com/abisarvepalli/nodejs-chaincode-bootstrap/tree/toolchain-chaincode) |
| Fabric | GoLang | [![Deploy To Bluemix](https://console.ng.bluemix.net/devops/graphics/create_toolchain_button.png)](https://console.ng.bluemix.net/devops/setup/deploy/?repository=https://github.com/abisarvepalli/blockchain-toolchain&branch=new-form&platform=go&bootstrapRepo=https://github.com/abisarvepalli/chaincode-bootstrap.git&env_id=ibm:yp:u\s-south) | [GoLang Sample Chaincode](https://github.com/abisarvepalli/chaincode-bootstrap/tree/toolchain-chaincode) |