# gitops-argocd

Create the argocd apps-of-apps:

```
argocd app create apps \
  --repo https://github.com/spectrocloud/gitops-argocd.git \
  --path capi-clusters \
  --dest-name in-cluster \
  --dest-namespace argocd \
  --sync-policy automated \
  --auto-prune
```

## Add a new Cluster example

To add additional capicluster, e.g: _team3_, perform the following operations:
- Copy `cluster-eks-3.yaml` directory
- Make any modificaitons as necessary

