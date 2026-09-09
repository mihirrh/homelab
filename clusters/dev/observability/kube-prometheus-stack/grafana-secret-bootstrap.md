# Bootstrap secret — create ONCE manually then never commit the password to Git.
#
# Run this once before pushing the observability stack:
#
#   kubectl create namespace monitoring
#   kubectl create secret generic grafana-admin-secret \
#     --namespace monitoring \
#     --from-literal=admin-user=admin \
#     --from-literal=admin-password='<strong-password>'
#
# The HelmRelease references this secret so Grafana picks up the credentials
# at install time. Flux manages the HelmRelease; you manage the Secret out-of-band.
#
# If the secret doesn't exist before Helm installs, Grafana will fail to start.
# Run the kubectl command above BEFORE pushing this stack for the first time.
