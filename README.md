# Argo CD

> Install and configure Argo CD

```bash
admin
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```

Fix ingress **ERR_ TOO_ MANY_ REDIRECTS** 

```yaml
spec:
  containers:
  - command:
    - argocd-server
    - --insecure # <-- this thing needs to be added
```

[Blogs and Presentations](https://github.com/argoproj/argo-cd#blogs-and-presentations)
