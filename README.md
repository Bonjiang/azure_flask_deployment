
# How to set up and deploy the application

##### Flask Initiation

First, use **'pip install flask'** to install the Flask. Then, create a python file **'app.py'** and templates to guide how the website would appear and function. For example, here, the names and titles are customized to your preference. 

##### Install Azure CLI 

To deploy, install Azure CLI using **'curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash'** This is done in one command or can be done step-by step following the [instructions](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt). Following that, we want to test that it installed with **'az'**. Following would be **'az login --use-device-code'**, which would prompt a code to be copied and pasted in the Microsoft login pop-ups. 

##### Specific to our class

Get azure student subscription ID **'az account list --output table'** and this would show three subscription IDs to which we would copy the Azure for Students one and paste in the following command **'az account set --subscription [yoursubscriptionID]. This would change the subscription id. 

##### Create a new resource group

Go into the azure web sportal and under 'Navigate' in the home page, select 'Resource groups' to create a new resource group and make sure the subscription is for 'Azure for Students'. You can also check the group names using **'group list'** to see if it already exists.

##### Create the azure web app 

The **'az webapp up --resource-group <groupname> --name <app-name> --runtime <PYTHON:3.9> --sku <B1>'** command is unique to you. The app name is specific. 

##### Deployment

To deploy, use **'az webapp up'** and this takes a while, especially if it's a first time. My application is (https://bonnie-504-flask.azurewebsites.net/)

