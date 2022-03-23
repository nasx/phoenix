# OpenShift Demo Builder

This project is currently a work in progress. The intent is to create a repository of helm charts deployed by ArgoCD via a dynamically generated/nested app of apps pattern. Using a global Helm Values file, users can pick and choose different components/products to build custom demos. Wherever possible, the components deployed will be automatically integrated.

## Installing

On an new OpenShift cluster, run the following command to install and configure the OpenShift GitOps operator (ArgoCD):

```shell
./setup/init.sh
```

All of the components will be deployed by default. Run the following command to bootstrap the environment and generate the nested app of apps structure.

```shell
helm upgrade -i -n umbrella-gitops bootstrap charts/bootstrap/
```