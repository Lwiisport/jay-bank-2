# Exercice 10 (repo 2) : extend a CI workflow (github actions).

voici mon nouveau `GitHub Actions` : 

```
name: Java CI

on:
  push:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Set up JDK 17
        uses: actions/setup-java@v3
        with:
          distribution: temurin
          java-version: '17'

      - name: Clean & test
        run: mvn clean test

      - name: Package project
        run: mvn package

      - name: Upload build artifacts
        uses: actions/upload-artifact@v4
        with:
          name: java-build
          path: target/
```

Ceci permet donc d'exécuter les commandes `mvn clean test`, puis `mvn package` et finalement une archive dans le dossier `target/`

Le workflow fonctionne correctement.
