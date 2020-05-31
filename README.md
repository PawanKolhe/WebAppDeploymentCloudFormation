# High-Availability Web App Deployment using CloudFormation

In this project, web servers are deployed for a highly available web app using CloudFormation.

---

> YAML `.yml` files contain the CloudFormation template body with declarations of what resources are to be created and their configuration. 

> JSON `.json` files contain the parameters to be passed to the script. 

> SHELL `.sh` files are helper scripts to enable easy create, update and delete operation on cloudformation stacks.

---

## Architechure Diagram

![Architecture Diagram](https://github.com/PawanKolhe/WebAppDeploymentCloudFormation/blob/master/Diagram.png)

## Deployment Instructions

### Prerequisites
- AWS CLI: https://aws.amazon.com/cli/
- AWS Account

### Commands

##### Create Stack
```sh
./create.sh <NAME-OF-STACK> <TEMPLATE-FILE> <PARAMETER-FILE>
```

##### Update Stack
```sh
./update.sh <NAME-OF-STACK> <TEMPLATE-FILE> <PARAMETER-FILE>
```

##### Delete Stack
```sh
./delete.sh <NAME-OF-STACK>
```
    
### Example
	# Creating stack
	./create.sh udagram-network network.yml network-params.json
	./create.sh udagram-servers servers.yml servers-params.json
	./create.sh udagram-bastion bastion.yml bastion-params.json
	
	# Creating stack
	./update.sh udagram-network network.yml network-params.json
	./update.sh udagram-servers servers.yml servers-params.json
	./update.sh udagram-bastion bastion.yml bastion-params.json

	# Deleting stack
	./delete.sh udagram-servers
	./delete.sh udagram-bastion
	./delete.sh udagram-network
