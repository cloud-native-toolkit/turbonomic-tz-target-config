# Turbonomic post install steps for targets configuration
This template 'turbonomic-tz-target-config.yaml' configures AWS, Azure, vSphere, Openshift and Instana targets, so that Turbonomic can provide appropriate action recommendations. Only Turbonomic deployed on AWS ROSA, Azure ARO and IBM ROKS clusters through TechZone are supported.

## Pre-requisites:
 - ROSA/ARO/ROKS cluster deployed through TechZone
 - Turbonomic is up and running
 - Valid Turbonomic license is applied
 - oc client on your workstation
 - You should have cluster-admin access on the cluster
 - Login to the OCP Cluster

## Steps to deploy the use cases:

1) Clone this repository: `git clone https://github.ibm.com/gsi-labs/turbonomic-tz-target-config.git'
2) Change directory to the cloned direcrtory: `cd turbonomic-tz-target-config.git`
3) Run below command:

`oc new-app -f turbonomic-tz-target-config.yaml -p TURBO_NAMESPACE=<Turbonomic-namespace> -p TURBO_ADMIN_USER=<Turbonomic-User> -p TURBO_PASSWORD=<Turbonomic-password>`

Wait for ~30 minutes for required actions to appear in Turbonomic console.
