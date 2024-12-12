# Cloud Dev with Azure Cloud Shell

* Azure got highly connected data centers with Shell environment. 
* Inside Shell, got access for:
  1. Network
  2. Data Center
  3. proper Roles
  4. Storage
  5. can deploy PaaS (Platform as a Service) app

* Can choose which one you're more familiar to:
  * Bash commands
  * PowerShell commands

## How to access Microsoft Azure?
https://portal.azure.com/?quickstart=true#home

## Options to consider when opening Shell:
1. Storage? will storage be needed? if yes:
   * Choose a Storage account subscription
   * Setup Mount storage account
     * for now, I chose "we will deploy for you"

2. whether will use Existing Private Virtual Network or not

## Built-in Commands at Azure Cloud Shell

| Command            | Description                     |
|--------------------|---------------------------------|
| `az`               | to call Azure CLI               |
| `az help`          | to learn more about Cloud Shell |
| `python --version` | can run Python in Azure         |

## Icons at Azure Cloud Shell

### 4. [to Move / Upload / Download Data](https://github.com/maryjess/cloud/issues/19)

### 6. `{}` to Open Editor
* Allows to Edit Project
   
#### How to Close Editor?
* Right-click the menu on top right --> Select Close Editor
* Alternatively, Ctrl + Q (keyboard shortcut)