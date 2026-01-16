# Exercice 7 (Repo 2): Add test dependencies and explore the Maven lifecycle

Les phases `clean` `test` et `package` sont exécuté.
`clean` nettoie le dossier `/target`.
`test` compile les classes et les tests et exécute les tests.
`package` compile le projet, exécute les tests et génère une archive du projet. 

le dossier `/target` contient les classes, les sources généré, des dossiers pour les archives et le statut de maven, des reports `sunfire`, les classes de tests ainsi qu'une archive du projet.


`mvn test` va seulement exécuté les tests unitaires là où `mvn verify` va vérifier le projet dans son ensemble.

`mvn test` génère l'archive, `mvn verify` valide de l'archive est correct.
