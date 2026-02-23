# cnhash

**cnhash** est un projet Java modulaire utilisant **Spring Boot** et **Maven**.  
Le projet est structuré en modules Maven :

- `cnhash-core` : contient la logique métier et les classes utilitaires.
- `cnhash-api` : contient l’API REST, basée sur Spring Boot, exposant les fonctionnalités du core.

---

## Structure du projet

cnhash/
├─ pom.xml # POM parent
├─ core/ # Module core
│ ├─ pom.xml
│ └─ src/main/java/... # Classes métier
├─ api/ # Module API
│ ├─ pom.xml
│ └─ src/main/java/... # Application Spring Boot et contrôleurs

---

## Prérequis

- Java 21
- Maven 3.6.3+
- Un IDE compatible Java (IntelliJ IDEA, Eclipse, VSCode...)
- (Optionnel) Postman ou tout autre client REST pour tester l’API

---

## Compilation et Build

Pour compiler et installer les modules dans le repository local Maven :

mvn clean install

Cela build:

Le module core et installe le JAR dans le repository local (~/.m2/repository/chijouProjects/core/).

Le module api et installe son JAR (~/.m2/repository/chijouProjects/api/).

## Lancer l’API

Pour démarrer le serveur Spring Boot (module api):

cd api
mvn spring-boot:run

Ou en exécutant directement le JAR:
java -jar target/api-0.0.1-SNAPSHOT.jar

Le serveur sera disponible par défaut sur http://localhost:8080.

## Tests

Chaque module contient des tests unitaires.
Pour exécuter tous les tests:

mvn test

## Dépendances principales

Spring Boot 3.5.11 : framework principal pour l’API

JUnit 4 / 5 : pour les tests unitaires

Lombok : pour générer automatiquement getters/setters, constructeurs, etc.

## Prochaines étapes

Ajouter les classes métier dans core

Ajouter les contrôleurs REST dans api

Configurer la connexion à la base de données si nécessaire

Ajouter Swagger pour documenter l’API

## Contact

Projet créé par DUBOIS ROGER CHIJOU NENGOU
Email : duro.chijou@gmail.com