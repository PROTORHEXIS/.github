# PROTORHEXIS — Référentiel de collaboration de l'organisation (proposition)

[简体中文 / English](../COLLABORATION_BASELINE.md) · **Français** · [Español](COLLABORATION_BASELINE.es.md) · [Русский](COLLABORATION_BASELINE.ru.md)

> État : `PROPOSED` · Dépôt concerné : `.github` public de l'organisation · Responsables : propriétaire de l'organisation ou mainteneurs désignés.
>
> Ce document décrit le périmètre et les conditions d'activation des modèles communs. Il ne constitue ni une spécification produit de référence, ni une décision d'architecture approuvée, ni une configuration effective de sécurité.

## Objectif et contenu

Fournir une méthode claire et vérifiable pour signaler les problèmes, proposer des changements, soumettre des PR et coordonner les divulgations de sécurité, sans retirer à chaque dépôt la maîtrise de son code, de ses règles, de son CI et de ses publications.

| Fichier | Rôle | Limite |
| --- | --- | --- |
| [CONTRIBUTING.md](CONTRIBUTING.fr.md) | Contributions, confidentialité et preuves | Ne garantit pas l'accueil de contributions externes |
| [PULL_REQUEST_TEMPLATE.md](../../PULL_REQUEST_TEMPLATE.md) | Portée, autorisation, risques, vérification et HOLD | Ne remplace pas les revues ou contrôles obligatoires |
| [bug_report.yml](../../.github/ISSUE_TEMPLATE/bug_report.yml) | Formulaire de défaut | Pas de détails sensibles en public |
| [change_proposal.yml](../../.github/ISSUE_TEMPLATE/change_proposal.yml) | Proposition de recherche, d'ingénierie ou de gouvernance | Une proposition n'est pas une règle approuvée |
| [config.yml](../../.github/ISSUE_TEMPLATE/config.yml) | Autorise les Issues libres | Peut être remplacé localement |
| [SECURITY.md](SECURITY.fr.md) | Divulgation responsable | Aucun canal privé ni SLA inventé |

## Héritage et activation

Les fichiers communautaires pris en charge dans le dépôt **public `.github`**, sur sa branche par défaut, peuvent servir de modèles aux dépôts de l'organisation **publics ou privés** qui ne possèdent pas leur propre fichier correspondant. Un fichier propre au dépôt a priorité. Ces modèles ne créent pas de permissions, de protections de branches ou d'obligations de revue au niveau technique.

Tant que le contenu se trouve sur une branche séparée dans une **Draft PR**, il reste une proposition : **aucune activation automatique**. Seule son intégration à la branche par défaut peut entraîner l'héritage. Un `AGENTS.md` dans le dépôt `.github` n'est pas automatiquement transmis aux autres dépôts ; les agents doivent lire les instructions et décisions réellement applicables à leur dépôt de travail.

## Autorité et interprétation des preuves

1. Les spécifications et décisions approuvées, le code, les migrations, les tests et les faits liés à des commits restent sous la responsabilité de leurs dépôts respectifs.
2. Distinguer `target` (objectif), `implementation` (réalisation) et `gap` (écart). Un objectif n'est pas une réalisation prouvée.
3. Distinguer `PROPOSED / ACCEPTED / IMPLEMENTED / STATIC_VERIFIED / LOCAL_PASS / REMOTE_CI_PASS / UNVERIFIED / BLOCKED / HOLD`. Une vérification non réalisée est `NOT RUN`, jamais `PASS`.
4. Une validation locale avec environnement et preuves identifiés n'est pas un contrôle GitHub Actions réussi. Une panne de CI, de quota ou de facturation doit être signalée séparément.
5. Les données de dépôts privés, recherches non publiées, configurations de droits et journaux de sécurité ne deviennent pas publics du seul fait que les modèles se trouvent dans un dépôt public.

## Décisions préalables à l'activation

- [ ] Examiner tous les textes publics pour détecter des informations privées ou non autorisées.
- [ ] Valider un véritable canal de communication confidentiel pour la sécurité, sans inventer d'adresse électronique ou de fonctionnalité activée.
- [ ] Vérifier l'héritage et la priorité des modèles locaux dans un dépôt public et un dépôt privé ; sinon déclarer `NOT VERIFIED`.
- [ ] Vérifier réellement le rendu GitHub des deux formulaires Issue, leurs champs obligatoires et leurs avertissements.
- [ ] Confirmer que les instructions des projets, revues, CI, commits exacts, HOLD et règles de publication restent applicables.
- [ ] Obtenir l'accord explicite du propriétaire pour l'effet de portée inter-dépôts avant de rendre la PR fusionnable, puis respecter les règles de revue du dépôt.
