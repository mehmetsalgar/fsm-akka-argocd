helm upgrade --install argocd . --create-namespace -n argocd
helm upgrade --install argocd . --create-namespace -n argocd --set projects.enabled=true

helm delete argocd -n argocd

username: admin
password: -> inside of the k8s secret -> "initial admin secret"

https://learn.microsoft.com/en-us/azure/key-vault/secrets/multiline-secrets?source=recommendations
az keyvault secret set --vault-name "fsmakkaKeyVault" --name "config" --file "config.txt"