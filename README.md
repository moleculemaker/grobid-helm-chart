# grobid-helm-chart
Helm chart for running Grobid in a Kubernetes cluster

Defaults to version 0.7.3

## References
* Docker image: [grobid/grobid](https://hub.docker.com/r/grobid/grobid)
* Based on the Docker Compose recipe: [ReactionMiner_v2](https://github.com/maszhongming/ReactionMiner/tree/ReactionMiner_v2)


## PSA: Always check Pod `AGE` after deploying
You may need to delete the running Pod to trigger a new Pod to be created with the new config.


## Installing the Helm chart
Whether you are running Kubernetes locally on your laptop or remotely in a cluster, you can use the following to run grobid using this Helm chart

To change the existing application in your cluster, you can use the following command:
```bash
$ helm upgrade --install grobid -n <namespace> .
```

This will overwrite the configuration of the instance in your cluster.

This example is currently not configured to use an Ingress Controller.

