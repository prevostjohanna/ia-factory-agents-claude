# Propale : module ROI, exemple, template

## Module ROI détaillé

Un ROI vide ou truffé de `[À VALIDER]` ne convainc personne ; un chiffre inventé tue la crédibilité de toute la propale. Entre les deux :

- Si l'appel contient de vrais chiffres (CA, temps, volumes), les utiliser en priorité.
- Sinon, poser des **hypothèses explicites et assumées** (volumes, panier, taux de conversion), chacune étiquetée « hypothèse : à figer au démarrage sur les données réelles ».
- **Ancrer par une recherche sourcée** ce qui peut l'être (benchmark sectoriel, coût de référence d'un poste) et citer la source. Si rien de défendable, `[À VALIDER]` sur CETTE variable seulement.
- **Formules visibles** : le client doit pouvoir refaire le calcul.
- **3 scénarios** (prudent / médian / ambitieux).

Un benchmark externe sert à **borner une hypothèse**, jamais à affirmer le résultat du client. Formuler au conditionnel et signaler l'écart entre benchmark générique et réalité client.

## Exemple (extrait)

> **Où tu en es.** « Aujourd'hui, chaque devis vous prend ~1 h, à la main, sur un book tarifaire papier. Sur 800 devis/an = **200 h**, un mois et demi à temps plein juste pour chiffrer. Ce n'est pas un problème de rigueur : c'est un problème de système. »
> **Les enjeux.** « Si rien ne change, ces 200 h se reproduisent, et un oubli de mention reste un risque juridique. À 50 €/h chargé = ~10 000 €/an financés sans le voir. »
> **Mon approche.** Pas une refonte : un agent de chiffrage branché sur votre book, livré en 6 semaines. Hors-périmètre : l'intégration Sage (phase 2).
> **Comment on bosse.** Phase 1 : 6 semaines, **9 000 € HT**. Option : tableau de bord de conversion, **+2 500 €**.
> **Pour démarrer.** « ROI : temps de chiffrage divisé par 3 + ~10 % de conversion (hypothèse à figer). La suite : 30 min avec votre direction pour valider et démarrer en novembre. On cale ça ? »

Un exemple réel de propale au format mini-site existe dans la page Notion de l'agent (bibliothèque d'agents) : diagnostic ≈40% avec verbatims, coût de l'inaction décliné en 3 coûts (commercial, dépendance, business), ROI en tableau d'hypothèses + 3 scénarios avec source citée, avant/après, un seul next step daté avec une urgence réelle reprise de l'appel.

## Template

```
1. OÙ TU EN ES (diagnostic, ~40%)
- Sa situation avec SES mots (verbatims) : « … »
- Ce qui bloque, en cascade : …
- Reframe déculpabilisant : « ce n'est pas vous, c'est le système »

2. LES ENJEUX (agiter le coût)
- Si rien ne change (3/6/12 mois) : …
- Coût du statu quo : [X h × Y €] = [Z €/an]  (hypothèse étiquetée si estimée)
- Ce qu'il peut gagner (ROI) : …

3. POURQUOI MON APPROCHE EST DIFFÉRENTE
- Vision unique : … · 3 piliers : … · 1 verbatim client : « … »
- Inclus : … · Hors-périmètre : …

4. QUI JE SUIS (court, relié à ses enjeux) : …

5. COMMENT ON BOSSE
- Étapes datées + livrables : …
- Budget : [phase] = [__ € HT] · option +/- : …

6. POUR DÉMARRER
- ROI projeté vs prix (3 scénarios, formules visibles) : …
- Avant / Après : …
- UN next step : « la suite logique, c'est … on cale ça ? »
```
