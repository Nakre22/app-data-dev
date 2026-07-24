<!-- ============================================================================
     EXEMPLE — page PROJET en grammaire v2 (directives @).
     Voir CLAUDE.md pour la référence complète du format.

     Règles clés :
       @meta / @header / @hero / @contact / @footer  → singletons (chrome de page)
       @section <id> "Libellé libre"                 → une section (ancre = id)
         - group: <Groupe de sidebar>                → champ de section
       @<palette>                                    → un bloc réutilisable
         @item <Nom>                                 → une entrée de liste
       #, ##, ###                                    → VRAIS titres H1/H2/H3
       :::                                           → bloc de texte libre
       @include <fichier.md>                         → inclusion multi-fichiers
       data/x.png  → /api/data/x.png (partagé) ou /api/data/<slug>/x.png si le
                     dossier du projet contient un sous-dossier data/ local
     ============================================================================ -->

@meta
- project_id: exemple
- project_slug: exemple
- primary_color: #1850c0
- heading_font: playfair

@header
- title: PROJET EXEMPLE
- subtitle: Sous-titre du projet
- logo: data/placeholder.png

@contact
- email: contact@exemple.fr

@section home "PROJET EXEMPLE"
- group: Home

@whyWhatHow
<img src="data/placeholder.png" align="right" width="180" alt="logo">

**why:** Pourquoi ce projet. Le texte accepte des [liens](https://exemple.fr) et du **gras**.
**what:** Ce que fait le projet.
**how:** Comment il le fait.

@section projecttracks "Project Tracks"
- group: Home

@tracks
@item Axe 1
- description: Description du premier axe de travail.
@item Axe 2
- description: Description du deuxième axe.

@section members "Membres"
- group: Members

@members
- description: Notre équipe pluridisciplinaire. Texte riche avec [liens](https://exemple.fr).

:::
Un bloc `:::` insère du texte libre n'importe où dans la section, y compris
entre deux items.
:::

@item Prénom Nom
- role: Chercheur·e
- email: prenom.nom@exemple.fr
- linkedin: https://linkedin.com/in/prenom-nom
- image: data/placeholder.png

@item Autre Personne
- role: Ingénieur·e
- email: autre@exemple.fr
- image: data/placeholder.png

@section documents "Documents & Publications"
- group: Productions

@documents
- description: Nos publications, en accès libre sur [HAL](https://hal.science/).

@item Titre de l'article
- type: Conference Paper
- author: A. Auteur — LIRIS
- venue: DISC 2025
- abstract: Résumé long de l'article. Peut être tronqué et déplié côté frontend.
- link: https://arxiv.org/...

@section events "Événements"
- group: News & Events

@events
@item Séminaire de rentrée
- date: 2026-03-20
- type: Conference
- venue: Amphi Gouy
- abstract: Description de l'événement (les événements sont triés à venir / passés).

@section relatedprojects "Projets liés"
- group: Miscellaneous

@relatedprojects
@item LIRIS (CNRS)
- link: https://liris.cnrs.fr/
- description: Laboratoire d'accueil de l'équipe.
