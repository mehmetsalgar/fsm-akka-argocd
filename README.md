helm upgrade --install argocd . --create-namespace -n argocd
helm upgrade --install argocd . --create-namespace -n argocd --set projects.enabled=true

helm delete argocd -n argocd

username: admin
password: -> inside of the k8s secret -> "initial admin secret"