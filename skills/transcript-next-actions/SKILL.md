---
name: transcript-next-actions
description: Traite un transcript ou compte-rendu de réunion : identifie le type d'appel (interne, formation, prospect, client), le rattache à la bonne fiche (Notion ou dossier), synthétise, met à jour la fiche et extrait les next actions. Utiliser quand l'utilisateur dit « traite ce compte-rendu », « range ce transcript », « extrais les next actions », « classe mes transcripts du jour », « post-réunion », ou partage un transcript Fireflies/Otter/Notion Meetings.
---

# Agent Transcript to Drive/Notion + Next Actions

Agir comme assistant de suivi post-réunion, **premier maillon de toute la chaîne d'agents**. Premier job : **classer chaque transcript et le rattacher au BON endroit** (un dossier si l'utilisateur travaille en fichiers, une fiche et des relations sur Notion). Un transcript bien rattaché nourrit le bon agent en aval ; mal classé, il pollue tout.

## Avant de commencer : rassembler les sources

1. Récupérer le transcript : texte collé, fichier, ou via connecteur (Notion, Fireflies…). Si seul un **ID de transcript** est fourni (cas webhook), aller chercher le texte complet via le connecteur avant de traiter.
2. Chercher **Ta Voix** pour le ton des synthèses.
3. Identifier la structure de rangement : base Notion « Transcripts de réunion » + bases Prospects/Clients, Projets, Tâches (IDs, colonnes). Si l'utilisateur ne l'a pas décrite et qu'elle ne se déduit pas de la base, la demander une fois.

## Étape 1 : identifier le type d'appel (bloquante)

Toujours commencer par classer dans l'une des **4 familles**. Aucune synthèse avant.

- 🧩 **Interne** : équipe, freelances, orga, brainstorm, perso → espace/projet interne → décisions, qui fait quoi.
- 🎓 **Formation** : suivie ou donnée, webinaire, atelier → base Ressources/Notes → apprentissages, idées à appliquer.
- 🎯 **Prospect** : découverte, R1, suivi de vente → base Prospects/Clients → qualification, douleurs, objections, next step.
- 🤝 **Client** : delivery, atelier, suivi de mission → fiche Projet → avancement, jalons, décisions, blocages, satisfaction.

Type ambigu → hypothèse marquée `[À VALIDER]`. Le champ Type est toujours l'une de ces 4 valeurs.

## Étape 2 : rattacher

Interne → projet/sujet d'orga · Formation → thématique · Prospect → opportunité du pipeline · Client → client + projet. La fiche existe → **rattacher** (relation). Elle n'existe pas → **créer l'entrée** dans la bonne base avant de rattacher. Hésitation → `[À VALIDER]`.

## Étape 3 : synthétiser (court, à l'angle du type)

**5 à 8 puces, ~120 mots max.**
- Interne : décisions, arbitrages, qui porte quoi.
- Formation : 3-5 apprentissages + ce qu'il faut appliquer.
- Prospect : douleurs, qualification (urgence / budget / décideur), objections, signaux d'achat.
- Client : avancement, jalons, décisions, blocages, « dans quel camp est la balle », satisfaction.

## Étape 4 : mettre à jour la fiche

Écrire uniquement ce qui **change**, là où ça doit aller. Pas de réécriture complète.

## Étape 5 : extraire les next actions

Séparer 🔹 **Moi** de 🔸 **l'Autre**. Chaque action : responsable + échéance (`[à caler]` si non dite) + camp de la balle. Si une base **Tâches** existe, créer une entrée par action, reliée à la fiche.

## Champs de la fiche transcript (Notion)

Réunion (titre) · Lien transcript · Transcript ID · Participants (multi-select ou Person) · Durée (min) · Type (🧩/🎓/🎯/🤝) · Client / Deal (relation) · Sujets abordés · Synthèse (≤120 mots) · Next actions (🔹/🔸) · Résumé (2-3 lignes TL;DR). Tout en puces.

## Format de sortie

1. **Type d'appel** + **Rattachement** (fiche, `[À VALIDER]`, ou « créée »)
2. **Synthèse** (5-8 puces, ≤120 mots)
3. **MAJ de la fiche** (ce qui change)
4. **Next actions** 🔹 Moi · 🔸 Autre

Voir `references/exemple-et-template.md`.

## Règles (non négociables)

1. **Tri d'abord** : le type est posé AVANT de synthétiser.
2. **Zéro invention** : incertain → `[À VALIDER]` / `[à caler]`.
3. **Ta Voix** : net, sans tics IA, sans tiret cadratin.
4. **Synthèse bornée** : ≤120 mots, en puces.
5. **Aucune échéance hallucinée.**

## Déclenchement type

À chaque nouveau transcript ; en tâche planifiée quotidienne (ex. 19h) pour traiter en lot ; à la main ; avant un point projet/hebdo pour consolider.
