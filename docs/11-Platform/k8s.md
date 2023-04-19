---
title: Setups access to k8s cluster
sidebar_position: 4
---


# Setup Access to your Kubernetes Cluster:

## 1. For AWS

**Step 1:** Humalect creates an EKS cluster in your AWS account.
**Step 2:** It then configures the IAM roles based on the granted privileges, acting as a layer on top of the created EKS.
**Step 3:** User can access their kubernetes cluster via commands mentioned below or User Interface. 

### Commands:

```
export assumed_role_arn=<ask-humalect-team-for-this>
export external_id=<ask-humalect-team-for-this>
export cluster_name=<name-of-your-cluster>

region="${AWS_DEFAULT_REGION:-ap-south-1}"
aws_credentials=$(aws sts assume-role --role-arn $assumed_role_arn --role-session-name "terraform" --external-id $external_id --output json)
export AWS_ACCESS_KEY_ID=$(echo $aws_credentials|jq '.Credentials.AccessKeyId'|tr -d '"')
export AWS_SECRET_ACCESS_KEY=$(echo $aws_credentials|jq '.Credentials.SecretAccessKey'|tr -d '"')
export AWS_SESSION_TOKEN=$(echo $aws_credentials|jq '.Credentials.SessionToken'|tr -d '"')
aws eks update-kubeconfig --region $region --name $cluster_name --role-arn $assumed_role_arn
```
### Values and Flags:

| values                | description | 
| --------------------- | ----------- | 
| assumed_role_arn      |  The Amazon Resource Name (ARN) and the assumed role ID, which are identifiers that you can use to refer to the resulting temporary security credentials. <br/><br/>For example, you can reference these credentials as a principal in a resource-based policy by using the ARN or assumed role ID. The ARN and ID include the RoleSessionName that you specified when you called AssumeRole.           | 
| external_id           |    A unique identifier that might be required when you assume a role in another account. If the administrator of the account to which the role belongs provided you with an external ID, then provide that value in the ExternalId parameter.          |
| cluster_name          |  Name of the cluster           | 
| AWS_ACCESS_KEY_ID     |   Specifies an AWS access key associated with an IAM user or role.<br/><br/>If defined, this environment variable overrides the value for the profile setting aws_access_key_id. You can't specify the access key ID by using a command line option.          | 
| AWS_SECRET_ACCESS_KEY |       Specifies the secret key associated with the access key. This is essentially the "password" for the access key.<br/><br/>If defined, this environment variable overrides the value for the profile setting aws_secret_access_key. You can't specify the secret access key ID as a command line option.      | 
| AWS_SESSION_TOKEN     |  Specifies the session token value that is required if you are using temporary security credentials that you retrieved directly from AWS STS operations. For more information, see the Output section of the assume-role command in the AWS CLI Command Reference.<br/><br/>If defined, this environment variable overrides the value for the profile setting aws_session_token. |                    


[More details here - 1](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html)

[More details here - 2](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html)

<br/>


| flags    | description |
| ------ | ----------- |
| --role-arn          | (string) --role-arn is the role which will be used by aws-iam-authenticator when you run kubectl to get a token and is only injected in to the generated config; it is not used for fetching EKS resources in any way by the command.    <br/><br/>The Amazon Resource Name (ARN) of the role to assume.|
|  --role-session-name | (string)   An identifier for the assumed role session.<br/><br/>Use the role session name to uniquely identify a session when the same role is assumed by different principals or for different reasons. In cross-account scenarios, the role session name is visible to, and can be logged by the account that owns the role. The role session name is also used in the ARN of the assumed role principal. This means that subsequent cross-account API requests that use the temporary security credentials will expose the role session name to the external account in their AWS CloudTrail logs. <br/><br/>The regex used to validate this parameter is a string of characters consisting of upper- and lower-case alphanumeric characters with no spaces. You can also include underscores or any of the following characters: =,.@-         |
| --external-id       | (string)   A unique identifier that might be required when you assume a role in another account. If the administrator of the account to which the role belongs provided you with an external ID, then provide that value in the ExternalId parameter. This value can be any string, such as a passphrase or account number. A cross-account role is usually set up to trust everyone in an account. <br/><br/>Therefore, the administrator of the trusting account might send an external ID to the administrator of the trusted account. That way, only someone with the ID can assume the role, rather than everyone in the account. For more information about the external ID, see How to Use an External ID When Granting Access to Your AWS Resources to a Third Party in the IAM User Guide . <br/><br/>The regex used to validate this parameter is a string of characters consisting of upper- and lower-case alphanumeric characters with no spaces. You can also include underscores or any of the following characters: =,.@:/-         |
| --output            |             |
| --region            |             |


[More details here](https://awscli.amazonaws.com/v2/documentation/api/2.0.33/reference/sts/assume-role.html)


## 2. For Azure
**Step 1:**


### Commands:

```
az login --user <me@myCompany.com> -password <myPassword>

```
[More on az login](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli)

```
# change the active subscription using the subscription ID
az account set --subscription <your-subscription-id>
```
[More on az account set](https://learn.microsoft.com/en-us/cli/azure/manage-azure-subscriptions-azure-cli#change-the-active-subscription)
```
# Get access credentials for a managed Kubernetes cluster
az aks get-credentials --resource-group humalect-resources --name <your-cluster-name>
```
### Required Parameters
*--name -n*
Name of the managed cluster.

*--resource-group -g*
Name of resource group. You can configure the default group using `az configure --defaults group=<name>`.

[More here](https://learn.microsoft.com/en-us/cli/azure/aks?view=azure-cli-latest#az-aks-get-credentials-examples)





### Troubleshooting
Need help? [Contact](./../Contact-us/reach-out-to-us) us

