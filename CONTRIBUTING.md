# Contribuer

Ces règles s'appliquent par défaut à tous les dépôts de l'organisation
TechTown. Un dépôt qui a de bonnes raisons de s'en écarter documente les
siennes dans son propre `CONTRIBUTING.md`, qui prend alors le dessus.

## Branches et pull requests

Rien ne part directement sur `main` : on passe par une branche et une pull
request, même pour un changement d'une ligne. La PR sert de trace de la
décision autant que de relecture.

Nommage des branches : `<type>/<sujet-court>`, par exemple
`feat/export-pdf`, `fix/timezone-facture`, `chore/bump-node`.

## Messages de commit

[Gitmoji](https://gitmoji.dev) suivi du format
[Conventional Commits](https://www.conventionalcommits.org/fr/) :

```
✨ feat: ajoute l'export PDF des factures
🐛 fix: corrige le décalage de fuseau horaire
♻️ refactor: extrait la validation dans un module dédié
⬆️ chore: passe Astro en 7.2
📝 docs: documente la procédure de déploiement
```

Le corps du message explique le *pourquoi* — le *quoi* se lit dans le diff.

## Labels

Quatre labels sont communs à tous les dépôts de l'organisation :

| Label | Usage |
|---|---|
| `dependencies` | Mise à jour de dépendances |
| `automated` | Ouvert par un bot, pas par un humain |
| `ci/cd` | Pipelines, workflows, déploiement |
| `terraform` | Infrastructure |

Chaque dépôt reste libre d'ajouter les siens.

## Intégration continue

La CI doit être verte avant merge. Si un job échoue pour une raison sans
rapport avec le changement, dis-le dans la PR plutôt que de le contourner
en silence.

## Dépendances

Les mises à jour sont proposées automatiquement par Dependabot. Les
montées de version majeure méritent un coup d'œil aux notes de version
avant merge — le vert de la CI ne couvre pas ce qui n'est pas testé.
