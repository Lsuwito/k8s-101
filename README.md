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


## Kustomize
Use [Kustomize](https://www.digitalocean.com/community/tutorials/how-to-manage-your-kubernetes-configurations-with-kustomize) to configure k8s objects differently for each environment. Keep the common configuration in the base.

## Other Declarative GitOps Continuous Delivery Alternatives:
- [FluxCD](https://fluxcd.io/) 
- [Jenkins X](https://jenkins-x.io/)





