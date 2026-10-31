# Contribuer à PROTORHEXIS

[简体中文 / English](../../CONTRIBUTING.md) · **Français** · [Español](CONTRIBUTING.es.md) · [Русский](CONTRIBUTING.ru.md)

Nous accueillons les signalements de problèmes, les pistes de recherche, les discussions de conception, les améliorations documentaires et les contributions au code, selon les règles de chaque dépôt. Ce guide est un **cadre de contribution par défaut** : il ne signifie pas que tous les dépôts acceptent des contributions extérieures.

## 1. Vérifier le périmètre et les autorisations

1. Lire les fichiers `README.md`, `CONTRIBUTING.md`, `AGENTS.md` et les politiques de sécurité du dépôt concerné, lorsqu'ils existent.
2. Vérifier si les Issues, Pull Requests ou contributions externes sont acceptées. Ne révéler ni contenu, ni configuration, ni droits d'accès d'un dépôt privé.
3. Les règles propres au dépôt, les spécifications et décisions approuvées, les protections de branches et les validations existantes priment sur ces conseils généraux. En cas de conflit, demander une décision aux responsables.
4. Rechercher les discussions existantes. Pour un changement d'architecture, d'interface, de gouvernance, de traitement des données ou de communication publique, proposer d'abord le périmètre.

## 2. Présenter des changements vérifiables

- Décrire dans une Issue les faits observés, le résultat attendu, la reproduction, l'impact et les preuves disponibles ; distinguer les suppositions.
- Garder les PR ciblées. Expliquer le but, les contrats concernés, les tests réellement exécutés, la compatibilité, les risques et le retour arrière.
- Distinguer la cible, l'implémentation actuelle et les écarts. Une vérification non exécutée est `NOT RUN` ou `UNVERIFIED`, jamais `PASS`.
- Lier les résultats de vérification à l'environnement, aux commandes et au commit exact. Un test local ne constitue pas une approbation de CI distante ni une autorisation de publication.
- Éviter les changements non liés. Toute migration de données, modification de droits, opération destructive ou divulgation sensible exige l'autorisation applicable.
- Ne jamais publier de secrets, données personnelles, journaux privés ou contenus non autorisés. Consulter la [politique de sécurité](SECURITY.fr.md) pour les vulnérabilités.

## 3. Revue et statuts

Les statuts `PROPOSED`, `IMPLEMENTED`, `STATIC_VERIFIED`, `LOCAL_PASS`, `REMOTE_CI_PASS`, `UNVERIFIED`, `BLOCKED` et `HOLD` représentent des niveaux différents. Une PR ne vaut pas approbation. Les revues, contrôles obligatoires, commits exacts, décisions `HOLD` et règles de publication du dépôt restent applicables.

## 4. Comportement collaboratif

Respecter les personnes, examiner les arguments avec rigueur et accueillir les désaccords étayés. Le harcèlement, la discrimination, la divulgation de données privées et les attaques personnelles sont incompatibles avec cette collaboration. Signaler les incidents par un canal approprié sans exposer publiquement des informations sensibles.
