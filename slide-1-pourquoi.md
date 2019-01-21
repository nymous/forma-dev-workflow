# 1. Quoi ? Pourquoi ? {bg=#2C3E50EE}

# 1.1 Quoi ?

* Présentation des outils utiles à tout projet de dev moderne

* Intégration de ces outils dans une chaîne

* Projet squelette

# 1.2 Pourquoi ?

* Travail plus fluide
* Cycle *développement => mise en production* raccourci
  * => feedback rapide
* Moins peur de faire des erreurs
  * petits incréments faciles à corriger/annuler
  * un workflow qui réduit les erreurs
  * la MEP devient la routine
* Process automatisé
  * => moins d'erreurs humaines

# 1.3 Le workflow

<div class="custom-image">

```{.render_dot}
digraph {

code [ label="Code code code..."];
pr [ label="Ouvrir une pull request" ];
code_review [ label="Relire le code 👀" ];
pr_accept [ label="Changements acceptés ! 💪" ];
pr_reject [ label="Changements refusés 😢" ];
tests [ label="Lint, tests... 🙏" ];
tests_accept [ label="Tests verts !" ];
tests_reject [ label="Tests rouge 😡" ];
docker [ label="Construction de l'image Docker 🐋" ];
deploy [ label="Déploiement en production ! 🚀" ];

code -> pr -> code_review -> pr_accept -> tests -> tests_accept -> docker -> deploy -> code
code_review -> pr_reject -> code
tests -> tests_reject -> code
}
```
</div>
