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

<div class="custom-svg">

```{.render_plantuml args="-Sbackgroundcolor=transparent -SdefaultFontSize=24 -SdefaultFontName=Raleway"}
@startuml

start

:Code code code...;
:Ouvrir une pull request;
(A)
:Relire le code 👀;
if (PR acceptée ?) then (oui)
  :Changements acceptés 💪;
else (non)
  :Changements refusés 😢;
  :Recommencer à coder...;
  (A)
  detach
endif

:Lint, tests;
if (Tests OK ?) then (oui)
  :Tests verts ! ✔;
else (non)
  :Tests rouge 😡;
  :Recommencer à coder...;
  (A)
  detach
endif

:Construction de l'image Docker 🐋;
:Déploiement en (pré-)production ! 🚀;

end

@enduml
```

</div>
