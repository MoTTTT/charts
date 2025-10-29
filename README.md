# charts

Custom Helm Charts for Podzone site

- static-site: A Helm chart to maintain a static site from git, on secured Apache

StaticSite uses hardened Apache Web Server with content sync with a GitHub repository, and https certificate sourced from LetsEncrypt.

The Helm Chart contains the following resources:

- clusterissuer.yaml: Set the issuer definition in values.yaml
- certificate.yaml: Set the certificate definition in values.yaml
- configmap.yaml: This loads a minimal httpd.conf file, with security hardening appropriate for a static site
- deployment.yaml: This spins up Apache, with a git-sync-sidecar, and uses the httpd.conf configmap
- ingress.yaml: Set the ingres definition in values.yaml
- service.yaml: Service endpoint for the deployment
- serviceaccount.yaml: Service Account for the deployment
