# Openshift to Kubernetes converter

Easily and quickly convert your RedHat Openshift workloads to standard kubernetes for clusters such GKE

Shifter has extensible methods for inputs and generators.

-----------------

## Processor

Processors are the converts from openshift to kubernetes.

-----------------

## Inputs

Inputs are readers for your existing Openshift application deployment methods

Currently supported inputs:


* **Yaml**

  Yaml input takes a standard OpenShift yaml file and changes certain api calls from OpenShfit specific to standard Kubernetes example: DeploymentConfig to Deployment

* **Templates**

  Template converter takes a Openshift template, converts it into kubernetes compatible resources and outputs given the format required.

* **Cluster**

  Cluster converter takes the resources deployed to a Openshift Namespace, converts those resources into kubernetes compatible resources and outputs given the format required. 

----------------

## Generators

Generators create new code based on your input to be used by standard Kubernetes distributions.

Currently supported generators:

* **Helm**

  Helm charts support the ability to create reusable charts that take input, this is a good fit from moving from Openshift Templates.

* **Yaml** 

  Create a standard yaml file for deployment, good for one off deployments such as inputting from yaml.

If you are interested in contributing, see [DEVELOPMENT.md](./DEVELOPMENT.md)

## Usage

### Yaml converter
```./shifter yaml --input input --output output --generator helm```

### Template converter
```./shifter template -i input.yaml -o <directory>```
