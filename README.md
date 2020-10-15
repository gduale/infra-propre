# Règle pour une infrastructure «propre»

* Tout doit être stocké dans git
* Tous les logs doivent être envoyés à syslog puis à ELK
* Tout doit être supervisé (et les intervalles des sondes doivent être cohérents)
* Il ne faut aucun log d'erreur système 
* Il ne faut aucun log d'erreur applicatif (ou alors non expliqué et tenir une base de référence de ces erreurs)
* On doit pouvoir déployer une VM, sa configuration et sa supervision de manière 100% automatique
* MaC : Monitoring As Code : Sensu par exemple
* Le DNS en automatique, dans git, git push et ça déploie les nouvelles entrées DNS
* Un outil de type IPAM avec API pour stocker les informations réseaux
* On doit pouvoir déployer son application, son code, juste en faisant "git push", le reste doit être automatique
  * Préciser (dans le projet ?) sur quelle brique logicielle doit tourner l'appli
* Utiliser un outil de type puppet ou ansible pour automatiser l'infra (+ terraform ?)
* La communication doit être autant que possible asynchrone (peu de réunion), discussion de sujet par ticket git sur des features, ou par mail
* Tout doit être documenté (c'est pas Machin qui doit savoir monter le LDAP) c'est soit du code soit de la doc, point.
  * La doc en markdown versionné dans git puis génération de page html (ou pdf) via pandoc ou mkdocs + CI pour mettre à dispo la doc en html
* Le code doit être commenté
* Best tool for the job : pas de stack ! Un choix de tool devrait être justifié
* Travailler avec la méthode Kabna (Trello / Jira)
* On doit pouvoir mettre en maintenance son application par du code
* Gestion des backups avec un outil open source dédié
* Pour la partie gestion du réseau : Software-defined networking
* Tous les identifiants et mots de passe accèssibles via navigateur web dans un Keepass like en https. (avec des ACL)
