# 16207

Purpose of this example is to reproduce incident https://github.com/argoproj/argo-cd/issues/16207

## How to

1. Create both AppProject
2. Configure the following variables:

```
ARGOCD_APPLICATION_NAMESPACES=argocd-team-one,argocd-team-two
ARGOCD_APPLICATIONSET_CONTROLLER_NAMESPACES=argocd-team-one,argocd-team-two
ARGOCD_APPLICATIONSET_CONTROLLER_ALLOWED_SCM_PROVIDERS=https://github.com # Or whatever
```

3. Start `make start-local`
3. Create both ApplicationSet.
4. Look at the applicationset logs. It must reconcile in loop