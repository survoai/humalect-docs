# Creating a new environment
## Environment
An environment refers to a Kubernetes namespace that is a completely isolated and self contained entity containing multiple application deployments and datasources.

 ## Prerequisites for creating an environment
 1. You should have a running cluster.
 2. You should be authorized to create an environment.

## Create Environment
1. To start creating an environment, go to Humalect's console's `dashboard` -> click on `Environment` -> click on `Create New Environment` button on the top right.
After following step 1, you will see this screen:
![create-env](./../../static/img/create-env.png)

2. Name the `environment`. Some possible options are dev, staging or prod
3. Select a `cluster` from the drop-down menu. This cluster will be used to host your environment. 
4. Write the name of the Kubernetes `namespace` inside which you would like to host your environment. if the namespace does not exist already, it will be automatically created for you.

After you have entered all the required necessities mentioned above, click on highlighted `Create Environment` button at the bottom and your environment will be created. Now you can host create multiple pipelines inside this environment.

### Troubleshooting
Need help? [Contact](./../Contact-us/reach-out-to-us) us

