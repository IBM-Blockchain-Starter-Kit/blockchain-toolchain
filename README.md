# Chaincode Toolchain Automation

The scripts defined in this project create a toolchain that automates development, testing and deployment of chaincode components used during an MVP.  

|[![Deploy To Bluemix](https://console.ng.bluemix.net/devops/graphics/create_toolchain_button.png)](https://console.ng.bluemix.net/devops/setup/deploy/?repository=https://github.com/IBM-Blockchain-Starter-Kit/blockchain-toolchain&branch=chaincode&platform=composer)| Create a Composer toolchain|   
|---------|----------|
|[![Deploy To Bluemix](https://console.ng.bluemix.net/devops/graphics/create_toolchain_button.png)](https://console.ng.bluemix.net/devops/setup/deploy/?repository=https://github.com/IBM-Blockchain-Starter-Kit/blockchain-toolchain&branch=chaincode&platform=go)| **Create a Go toolchain**|

# Pre-Deployment Requisites 

|Pre-Req|Description|How to|
|-------|-----------|------|
|Customer IBM Cloud account| Account where the toolchain will be created|N/A|
|Access to customer's IBM Cloud account| Your user ID should be added to the organization and space where pipeline will be created|TBD|
| Personal access token from IBM Cloud Git| Create a personal access token for the IBM Cloud Git service to allow pipeline to clone projects| Personal access tokens can be created [here](https://git.ng.bluemix.net/profile/personal_access_tokens) <br><br> **Note:** For more information on personal access token see [this](https://console.bluemix.net/docs/services/ContinuousDelivery/git_working.html#git_working) article.|


# Post-Deployment Requisites

* ... to be populated with information about blockchain network management  ...

# Template projects

|Project|Purpose|Cloned into IBM Cloud?|
|-------|-------|----------------------|
|chaincode-bootstrap| Contains template project for chaincode | Yes|

... to be populated with information about cross-organization repo usage ...


<br>
For more information about toolchains, see [Custom toolchains in one click with IBM Bluemix DevOps Services](https://developer.ibm.com/devops-services/2016/06/16/open-toolchain-with-ibm-bluemix-devops-services/).
