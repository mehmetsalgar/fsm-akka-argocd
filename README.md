helm upgrade --install argocd . --create-namespace -n argocd -f values-development.yaml -f values-gke.yaml
helm upgrade --install argocd . --create-namespace -n argocd -f values-test.yaml -f values-gke.yaml
helm upgrade --install argocd . --create-namespace -n argocd --set projects.enabled=true -f values-development.yaml -f values-gke.yaml

helm delete argocd -n argocd

username: admin
password: -> inside of the k8s secret -> "initial admin secret"
