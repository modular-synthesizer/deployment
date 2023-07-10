# Synple deployment

## Purpose

This project holds all the logic to deploy an entire environment of the Synple application suite. Provided an environment in the circle CI console, it can deploy all the needed applications to the provided cluster.

## Environment

### Environment variables

Environment variables needed for the deployment to work are :
* **KUBECONFIG_DATA_(DEV|PROD)** : the base64 encoded config file to connect to the kubernetes cluster where the application is deployed. End it with DEV for the kubernetes dev cluster, and PROD for the Kubernetes production cluster.

### Deployment variables

These variables are to be added when creating the job on circleci :
* __[required] environment__ : either `dev` or `prod` depending on the environment you want to deploy to.
