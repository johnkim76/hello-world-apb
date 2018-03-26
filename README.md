hello-world-apb
======================

An apb for deploying a simple [hello world](https://hub.docker.com/r/ansibleplaybookbundle/hello-world/) app that can bind to Postgres for testing purposes.

## What it does
* Deploys a bindable web app.

## Requirements

## Parameters
* NAMESPACE: Optional, default 'hello-world', Namespace to deploy the cluster in
* OPENSHIFT_TARGET: Required, target openshift deployment
* OPENSHIFT_TOKEN: Required, openshift token to authenticate as
* INVALID_NAMESPACE: Optional, default 'invalid_namespace', an invalid Namespace to create the route in
* TERMINATIONMSGPATHFILE: Optional, default '/dev/termination-log', path to the termination log used to output custom error message upon fatal erros
* enable_failure: Required, default `false`, Causes the provision to Fail (when set to `true`) demonstrating the custom error message feature on WebUI

## Running the application
`docker run -e "OPENSHIFT_TARGET=<openshift_target>" -e "OPENSHIFT_TOKEN=<token>" ansibleplaybookbundle/hello-world-apb provision`

## Tearing down the application
`docker run -e "OPENSHIFT_TARGET=<openshift_target>" -e "OPENSHIFT_TOKEN=<token>" ansibleplaybookbundle/hello-world-apb deprovision`
