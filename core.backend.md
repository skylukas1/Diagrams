# ops.k8s-staging

## Setup
1. Create application dir with Kubernetes manifests/helm chart
2. Create app in ArgoCD
```
argocd app create app1 --project staging --repo git@github.com:yardstik/ops.k8s-staging.git --path app1/ --dest-server https://kubernetes.default.svc --dest-namespace staging --auto-prune --sync-policy automatic
```
3. Enjoy


## Deployments
Need to automate version bumps, need GH action that can read yaml, and replace current version with new version, push and trigger deploy.
