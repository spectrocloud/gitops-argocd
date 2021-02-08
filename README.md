# gitops-argocd

Create the argocd apps-of-apps:

```
argocd app create apps \
  --repo https://github.com/spectrocloud/gitops-argocd.git \
  --path apps \
  --dest-name in-cluster \
  --dest-namespace argocd \
  --sync-policy automated \
  --auto-prune
```

## Add a new Jira team example

To add additional teams, e.g: _team3_, perform the following operations:
- Copy `apps/template/jira-team1.yaml` to `apps/template/jira-team3.yaml`
- Copy `jira-sm/overlays/team1` directory to `jira-sm/overlays/team3`

Make sure to replace all occurrences of _team1_ in any of the copied files above.
