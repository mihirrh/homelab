# The Argo project publishes its Helm charts at https://argoproj.github.io/argo-helm
# An HelmRepository named 'argocd' already exists in flux-system (pointing at the
# same URL), created by apps/argocd.  We reference that existing repo rather than
# creating a duplicate.
#
# If the argocd HelmRepository is ever removed, uncomment the block below:
#
# apiVersion: source.toolkit.fluxcd.io/v1
# kind: HelmRepository
# metadata:
#   name: argocd
#   namespace: flux-system
# spec:
#   interval: 6h
#   url: https://argoproj.github.io/argo-helm
