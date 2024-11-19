# Azure Settings
## Resource Group
Resource Group Name: cms1978

## SQL Database
DB name: cms1978

Server: cms1978.database.windows.net

DB region: Southeast Asia 

Admin login: cmsadmin

Admin password: CMS4dmin

Resource group: cms1978

DB workload env: Development

DB compute + storage: DTU - Basic

*Press the "Next: Networking" button, then select "Public Endpoint", and set both of the Firewall rules that appear to "Yes".*

*Set everything else to default*

*Run SQL queries in sql_scripts/ directory after completion, starting from the users table. Don't forget to take screenshots.*

## Storage Account
Resource group: cms1978

Storage account name: images1978

Advanced - Allow enabling anonymous access on individual containers: Enable

Advanced - Access tier: Cool

Network access: Enable public access from all networks (the default)

Create container named "images". Set its access level to Container.

From Security + networking > Access keys:

Blob Storage key: MhpJRYpQl9MGNWKiMnnS271VGYk6Gw2kRSXLb6OP5H8jZ4TMON5M1BMADLI2TIWfMibPzjY917VN+ASti3sqZA==

Blob connection string: DefaultEndpointsProtocol=https;AccountName=images1978;AccountKey=MhpJRYpQl9MGNWKiMnnS271VGYk6Gw2kRSXLb6OP5H8jZ4TMON5M1BMADLI2TIWfMibPzjY917VN+ASti3sqZA==;EndpointSuffix=core.windows.net

## Microsoft Entra ID
### App Registration
Name: cmsEntraID

*Who can use? "Accounts in any organizational directory (Any Microsoft Entra ID tenant - Multitenant) and personal Microsoft accounts (e.g. Skype, Xbox)"*

### Secret Creation
Secret description: cmsEntraIDsecret

Secret Key: 35693034-9af6-418b-899a-14861d8daef8

Client Secret: bq28Q~66UmEEyvHuOCWVEFwTw8GGjS4P91vOma1g

Application (client) ID: d70e7e78-0a9b-43ed-9c2f-979283ce4fe5

## Application
### OPTION 2: Web App (easier)

Name: udacitycms.azurewebsites.net

Runtime stack: Python 3.10

Pricing Plan: Free F1

*If you are getting a "Validation failed for a resource" error, pick a different region.*

## After creation:

*Settings -> Environment variables - Add the following variables (sample values are included, replace them with your values):*
BLOB_ACCOUNT: image11

BLOB_CONTAINER: images

BLOB_STORAGE_KEY: MhpJRYpQl9MGNWKiMnnS271VGYk6Gw2kRSXLb6OP5H8jZ4TMON5M1BMADLI2TIWfMibPzjY917VN+ASti3sqZA==

BLOB_CONNECTION_STRING: DefaultEndpointsProtocol=https;AccountName=images1978;AccountKey=MhpJRYpQl9MGNWKiMnnS271VGYk6Gw2kRSXLb6OP5H8jZ4TMON5M1BMADLI2TIWfMibPzjY917VN+ASti3sqZA==;EndpointSuffix=core.windows.net

SQL_SERVER: cms1978.database.windows.net

SQL_DATABASE: cms1978

SQL_USER_NAME: cmsadmin

SQL_PASSWORD: CMS4dmin

CLIENT_SECRET: bq28Q~66UmEEyvHuOCWVEFwTw8GGjS4P91vOma1g

SECRET_KEY: 35693034-9af6-418b-899a-14861d8daef8

CLIENT_ID: d70e7e78-0a9b-43ed-9c2f-979283ce4fe5

### Deployment Center

Source: GitHub

*Pick the repo that contains the starter files.*

## Setting up OAuth2
*At this point, your application should already be running. You should already be able to log in with username admin and password pass and you can create new posts or update existing ones.*

*The next part is getting the OAuth2 login to work.*

*Go to Microsoft Entra ID > App Registrations, click on the App Registration created earlier, and then pick Authentication from the left sidebar.*

### Microsoft Entra ID - Authentication - Add a Platform - Web

Redirect URIs: https://[IP ADDRESS FROM VM or WEB APP ADDRESS]/getAToken

logout URL: https://[IP ADDRESS FROM VM or WEB APP ADDRESS]/login
