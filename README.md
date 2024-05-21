# Immich

An opinionated Immich deployment using Kustomization.

## Assumptions / Requirements

These can be easily changed/replaced by appropriate substitutions.

- Intel GPU operator
- The last tested Immich version: `v1.105.1`
- Kubernetes `v1.29.4+` (tested on k3s with Traefik)
  - assumptions about kube-dns location and ingress controller location are based on this
- A *StorageClass* named `longhorn`
- Prometheus instance managed by prometheus-operator, named `prometheus` and running in the namespace named `monitoring`
- NFS accessible location with the photos, exported as `/mnt/pictures` on the IP address `192.168.1.100`
- A *ClusterIssuer* called `trusted-ca`
- DNS record pointing to the IP address of the ingress controller `fotos.home.arpa`
- Replace all occurences of `changeme` with some actual passwords
