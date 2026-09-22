# IA Factory Agents

Plugin Claude (Cowork / Claude Code) qui regroupe les **11 agents de la Bibliothèque d'agents IA Factory** sous forme de skills. Chaque skill reprend le prompt de l'agent (rôle, méthode, règles, format de sortie), avec les exemples et templates dans `references/`.

## Les skills

| Pilier | Skill | Ce qu'il fait |
|---|---|---|
| Socle commun | `transcript-next-actions` | Classe un transcript (interne / formation / prospect / client), le rattache à la bonne fiche, synthétise et extrait les next actions. Le 1er agent de tous. |
| Socle commun | `voc-voix-du-client` | Extrait verbatims, patterns, voix du marché et du produit d'un corpus client. Nourrit contenu et vente. |
| Acquisition Marketing | `strategie-edito` | Entretien de stratégie, puis idées scorées et calendrier de contenu rempli (sujet, pilier, funnel, angle, 3 hooks, format). |
| Acquisition Marketing | `redaction-contenu` | Écrit un contenu prêt à publier depuis une ligne du calendrier, dans Ta Voix, avec 3 hooks et 7 sweeps. |
| Acquisition Marketing | `lead-magnet-funnel` | Funnel complet : lead magnet (quiz de préférence) + page de capture + séquence de 9 emails. |
| Acquisition Marketing | `cas-clients` | Transforme un projet réussi en cas client Avant → Pont → Après (version site + post/carrousel). |
| Acquisition commerciale | `sales-prep` | Fiche stratégique + guide de call avant chaque R1 (SPICED, P.A.S.P., qui décide). |
| Acquisition commerciale | `closing-objections` | Après le RDV : objections, plan d'action commun (MAP), mail de suivi post-R1 et relances. |
| Acquisition commerciale | `propale` | Proposition commerciale qui fait signer : diagnostic, coût de l'inaction, ROI par hypothèses, un seul next step. |
| Delivery | `chef-de-projet` | Suivi de mission + récap client adapté au canal (email, Slack, espace client). |
| Pilotage | `cadrage-offre-pricing` | Décompose le CA cible en offres, structure l'échelle d'offres, price à la valeur. |

## Les chaînes

- **Contenu** : `voc-voix-du-client` → `strategie-edito` → `redaction-contenu`
- **Vente** : `lead-magnet-funnel` → `sales-prep` → `closing-objections` → `propale`
- **Delivery** : `transcript-next-actions` → `chef-de-projet` → `cas-clients`

## Docs de référence attendus

Les skills cherchent d'abord ces documents (fichiers du dossier de travail ou Notion via le connecteur) et **demandent ce qui manque** avant de produire. Aucun chiffre, verbatim ou cas client n'est inventé.

- **Ta Voix** (`tone-of-voice.md`) : utilisé par tous les skills
- **VoC** : page de synthèse Voix du Client, enrichie au fil de l'eau
- `services.md` (offres et prix) · `methode.md` · doc **Économie** (CA cible, charges)
- **Calendrier de contenu** (Notion) · **fiches Projets / Prospects / Clients / Tâches** (Notion)
- **Cas clients** + liens témoignages · `charte-graphique.md` (formats visuels)

Tes **Règles IA** vont dans les instructions globales de Cowork, pas dans le plugin.

## Connecteurs utiles

Pas obligatoires, mais ils rendent les skills autonomes :
- **Notion** : transcripts, fiches, calendrier, page VoC
- **Gmail / Slack** : brouillons de mails de suivi et de récaps (jamais d'envoi automatique)
- **Recherche web** : mini-veille prospect (`sales-prep`), benchmarks sourcés (`propale`)

## Installation

**Cowork** : importer le fichier `ia-factory-agents.plugin`.

**Claude Code** (repo privé, il faut avoir accès au dépôt) :

```bash
claude plugin marketplace add prevostjohanna/ia-factory-agents
```

```bash
claude plugin install ia-factory-agents@ia-factory
```

## Source

Généré à partir de la base Notion « 🤖 Bibliothèque d'agents ». Quand un agent évolue dans Notion, mettre à jour le `SKILL.md` correspondant et incrémenter la version dans `.claude-plugin/plugin.json`.
