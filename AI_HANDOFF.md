# AI HANDOFF PROTOCOL

## Définition

Un handoff est une passation structurée qui permet au fondateur ou à un autre collaborateur de reprendre un travail sans devoir relire l'intégralité d'une conversation antérieure.

Les conversations entre IA ne sont pas automatiquement synchronisées. #iC OS est le mécanisme documentaire commun : le handoff transmet le contexte utile, tandis que les fichiers officiels du dépôt portent l'état de référence.

## Quand produire un handoff

Un handoff est nécessaire à la fin d'un travail important, avant un changement de responsable, lorsqu'un blocage subsiste, lorsqu'une modification du dépôt a été effectuée ou lorsqu'une tâche doit être reprise dans une autre conversation.

Il peut être produit par le fondateur, ChatGPT, Claude, Gemini, Perplexity ou Codex. Il est destiné au prochain collaborateur désigné et au fondateur lorsque sa validation est requise.

## Règle de synchronisation

Avant de commencer ou reprendre une tâche, le collaborateur consulte `00_CURRENT_STATE.md`, `03_TASKS.md`, `07_DECISIONS.md` et les documents directement liés au périmètre. Il vérifie ensuite la branche, le commit ou la version de référence lorsque cela est applicable.

Un handoff ne remplace jamais la lecture de l'état officiel le plus récent. En cas de divergence, les fichiers validés de #iC OS et les décisions consignées dans `07_DECISIONS.md` prévalent sur le contenu d'une conversation ou d'un handoff ancien.

## Niveaux d'information

- **Information / fait :** élément vérifié, avec source lorsque nécessaire ;
- **Proposition :** recommandation ou hypothèse non validée ;
- **Décision :** élément explicitement validé par le fondateur et inscrit dans `07_DECISIONS.md` ;
- **État officiel :** situation actuellement enregistrée dans les documents de #iC OS.

Ces niveaux doivent rester séparés dans tout handoff.

## Informations minimales

Chaque handoff indique au minimum :

- l'émetteur, le destinataire, la date et le projet ou périmètre ;
- l'objectif et la version de référence consultée ;
- ce qui est réellement terminé ;
- les faits établis et leurs sources utiles ;
- les propositions non validées ;
- les décisions approuvées, avec leurs références ;
- les fichiers modifiés et le commit ou état Git pertinent ;
- les questions ouvertes, blocages et prochaines tâches précises.

## Format recommandé

```md
# AI HANDOFF

From:
To:
Date:
Project / scope:
Reference checked: branch / commit / documents

## OBJECTIVE

## COMPLETED

## FACTS ESTABLISHED

## PROPOSALS

## DECISIONS APPROVED

## OFFICIAL STATE TO UPDATE OR CONSULT

## FILES MODIFIED / GIT STATE

## OPEN QUESTIONS

## BLOCKERS

## NEXT TASKS

1.
2.
3.
```

## Cycle

**Consultation de #iC OS → Travail autorisé → Mise à jour de l'état officiel si nécessaire → Handoff → Reprise après nouvelle consultation de #iC OS**
