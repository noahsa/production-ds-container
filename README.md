# Production ML Container, No Kubernetes Knowledge

## Tools

1. OpenShift
2. S2I

## Steps

1. Login to OpenShift. Get command from `Copy login command` in the OpenShift web console.

    ```bash
    oc login --token=token --server=cluster_url
    ```

2. Create ML container

    ```bash
    oc new-build \
    https://github.com/noahsa/production-ds-container.git \
    --name=ml-image \
    --image-stream=openshift/python:3.8-ubi8
    ```
