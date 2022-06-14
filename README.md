# devops-environment

This project contains all the automation needed to provision the K8s cluster and all the supporting core infrastructure.

### Project Structure

You will find a readme document inside each responsibility folder with detailed information about its structure.

In order to keep all the things consistent and easy to manage this repository was structured in the following way:

* `deploy` folder contains owned deployments sync by FLUX CD

* `kubrnetes` folder contains any ad-hoc configuration and yaml files to support any additional deployments which
which are not covered by Terraform setup.

* `helm` folder contains custom [Helm Chart](https://helm.sh/) which will be used to deploy to k8s cluster.

* `terraform` folder contains custom modules and assembled environments which are ready to be deployed and serve its purpose.

* `scripts` this folder contains scripts and processes organized in folders intended to perform operations on different parts of the infrastructure.


On the other hand, a Dockerfile is included with the necessary tools to use and apply all this code, as well as a docker-compose to launch a container with the necessary configuration.

> docker compose run tools

## Environment Vars

* `AWS_ACCESS_KEY_ID` define a valid AWS ACCESS KEY ID with scopes to manage AWS ACCOUNT.
* `AWS_SECRET_ACCESS_KEY`: define a valid AWS SECRET ACCESS KEY paired with AWS_ACCESS_KEY_ID with scopes to manage AWS ACCOUNT.
