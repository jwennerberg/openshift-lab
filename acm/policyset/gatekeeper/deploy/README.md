# Deploy sample Gatekeeper policy-set

## Prerequisites

* ClusterSet named `container-platform`


## Deployment

Dry-run:
```
oc kustomize deploy/
```

Apply:
```
oc apply --kustomize deploy/
```


Add local-cluster to ClusterSet, add label:

```
oc label managedcluster/local-cluster cluster.open-cluster-management.io/clusterset=container-platform --overwrite
oc label managedcluster/local-cluster container-platform-managed=true
```


### Gatekeeper instance


