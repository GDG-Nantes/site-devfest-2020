---
key: gitops___une_mise_en_situation_un_peu_realiste_sur_kubernetes_avec_fluxcd
title: GitOps , une mise en situation un peu réaliste sur Kubernetes avec FluxCD
id: grExMwZ2uPDwi4m897vO
language: French
talkType: codelab
tags:
  - cloud-devops
complexity: Intermediate
speakers:
  - laurent_grangeau
  - ludovic_piot
draft: false
videoId: QecDAUbrlpc
---

# Abstract
T’en as assez des _talks_ qui déploient des _hello-world_ pour démontrer la pertinence de l’outil *younameit*.  
Ça tombe bien : ce qui nous intéresse, c’est plutôt d’essayer une mise en situation **DevSecOps** un peu réaliste.
On va donc construire pas à pas un scénario d’entreprise  avec une _dev team_, qui déploie / update / rollback des _WebApps_ Pokémon sur `Kubernetes` via des _charts_ `Helm`.  
Une seconde _dev team_ utilisera `Kustomize`, pour le même usage.  
Et côté _Ops_, on va aussi se préoccuper des enjeux de sécurité de la plateforme : ségrégations des droits des équipes, des flux réseau des WebApps, _patch management_ transparent sur la stack technique, métrologie, contrôle des activités sur le _cluster_.  
On va voir comment ces équipes **collaborent** entre elles au quotidien dans un _workflow_ **GitOps** qui s’appuie sur `Kubernetes`, `FluxCD`, `Azure DevOps`, et plein d’autres choses encore…

# Pré-requis
Ce _codelab_ assez dense nécessite :
* un _cluster_ `Kubernetes` (de préférence `AKS` chez **Azure**, celui qui est embarqué dans `Docker-desktop` pose problème)
* on travaille depuis un _container_ `docker` interactif dont l'image est ici : [thegaragebandofit/infra-as-code-tools:one-kubernetes](https://hub.docker.com/layers/172662032/thegaragebandofit/infra-as-code-tools/one-kubernetes/images/sha256-95723c5c9a016ec083c16fd596aab981ecf7e3c6bad797d3823e3e2647c8b3cb?context=repo), qui contient
  * az cli
  * git
  * kubectl
  * flux
  * kustomize
* on va aussi s'appuyer sur `github`
  * dépôts multiples
  * github actions
  * github artefacts
* on a une partie découverte de `azure devops` (nécessite un compte **Azure**)

Le détail des pré-requis et du _workshop_ sont ici : https://github.com/one-kubernetes/workshop
