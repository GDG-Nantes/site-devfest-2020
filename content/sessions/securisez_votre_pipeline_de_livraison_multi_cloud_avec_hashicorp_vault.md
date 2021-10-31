---
key: securisez_votre_pipeline_de_livraison_multi_cloud_avec_hashicorp_vault
title: Sécurisez votre pipeline de livraison multi-cloud avec HashiCorp Vault
id: iDnDhMBVtygPbh83ZIvB
language: French
talkType: conference
tags:
  - security
complexity: Beginner
speakers:
  - vincent_poilvert
draft: false
videoId: 3eICrAQu1qo
---

Je vois beaucoup de gens utiliser des secrets statiques écrits en dur dans leurs pipelines de déploiement pour s'authentifier auprès des fournisseurs cloud, ou pour se connecter sur des serveurs cibles à l'aide de ssh. La plupart du temps, le problème n'est pas résolu car il ne semble pas y avoir de solution facile, alors qu'il crée un risque critique pour la sécurité.

L'objectif de cette conférence est de montrer comment les pipelines de déploiement peuvent être sécurisés de manière unifiée entre les fournisseurs de cloud, en mettant en œuvre le principe du moindre privilège avec HashiCorp Vault. Il soulignera également les principaux avantages de l'utilisation de Vault, comme la politique de sécurité unifiée et les logs d'audit centralisés.

J'utiliserai l'exemple concret d'une entreprise qui a besoin de déployer une infrastructure sur son cloud privé et sur AWS. Cet exemple combinera des mécanismes d'authentification (AppRole, AWS), des stratégies Vault et des backends secrets (KV, AWS, SSH) pour créer un pipeline de livraison sécurisé et auditable.

Points clés à retenir :
* Les pipelines de livraison utilisant des secrets statiques avec des privilèges élevés constituent un risque de sécurité critique
* Le principe du moindre privilège peut être mis en œuvre dans des environnements multi-cloud
* Vault fournit une politique de sécurité unifiée et des logs d'audit centralisés
