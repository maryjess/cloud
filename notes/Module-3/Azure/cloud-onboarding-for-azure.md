# Cloud Onboarding for Azure Free Tier

## Microsoft Azure
There are many Resources for Microsoft:
* [Microsoft Learn](https://docs.microsoft.com/en-us/learn/)

* [Azure for Education](https://azure.microsoft.com/en-us/education/)

* [Azure Free Trial](https://azure.microsoft.com/en-us/free/)

---

### Using GitHub Actions with PyTest and Azure Cloud Shell

* Source code is [here](https://github.com/noahgift/azure-ml-devops)

#### Azure DevOps Workflow for Machine Learning

* Create Github repo (if not created)
* Open Azure Cloud Shell
* Create ssh-keys in Azure Cloud Shell
* Upload ssh-keys to Github
* Create scaffolding of the project (if not created):
   * Makefile
   * requirements.txt
   * python virtualenv
   * initial `hello.py` and `test_hello.py`
* run `make all` --> install, lint, and test code
* setup GitHub Actions in pythonapp.yml
* Commit changes and push to Github
* Verify Github Actions Test Software
* Run project in Azure Shell 

##### (not in PDF, but in source code)

* Push container to Azure Registery 
* Setup Azure Pipelines 
* Setup Kubernetes Cluster 
* Deploy to Kubernetes

---

> * This initial setup should allow for an exact CD workflow
> * Could be a starter kit to deploy code to an Azure PaaS (Platform as a Service) (see [diagram](https://github.com/maryjess/issues/17))
> * Could be imagined like this: [Continuous Delivery Diagram on Azure](https://www.github.com/maryjess/cloud/issues/16)