Logging Demo
------------

Copy of the original repo at: https://github.com/Azure-Samples/azure-voting-app-redis

Aim is to test out differences between Docker and Containerd logging.
It can also be used just to have an app that prodcued container logs.

Prerequisites
-------------

* Create an AKS cluster with two node pools: `nodepool1` and `nodepool2`
* Nodepool 1: 1.18.x (Docker/Moby)
* Nodepool 2: 1.19.x+ (Containerd)

Steps
-----

* Refer to steps here: https://github.com/clarenceb/moby-to-containerd-log-changes

Cleanup
-------

```sh
kubectl delete -f azure-vote-nodepool1.yaml -n app1
kubectl delete -f azure-vote-nodepool2.yaml -n app2

kubectl delete ns app1
kubectl delete ns app2
```
