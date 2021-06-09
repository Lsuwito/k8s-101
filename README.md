# Use GitOps Pull Methodology to Manage a K8s Cluster

## Concept

Developer -> Git <- Argo CD -> K8s Cluster

Developer commits application config/definition changes to Git. Argo CD detect the changes in Git, and sync the application in K8s.

## Requirements:
1. [Argo CD](https://argoproj.github.io/argo-cd/) - installed in the k8s cluster, it monitors application config/definition changes in Git repo, automatically deploy if out of sync.
2. Git repo containing the config/definition yaml files.
3. K8s Cluster (I use the [Docker Desktop K8s](https://docs.docker.com/desktop/kubernetes/#enable-kubernetes) on my local machine)

## Setup Argo CD
See the [Getting Started](https://argoproj.github.io/argo-cd/getting_started/) documentation.


Other alternatives:
- [FluxCD](https://fluxcd.io/) 
- [Jenkins X](https://jenkins-x.io/)





