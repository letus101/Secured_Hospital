# Gestion des Patients

## Description
Ce projet est une application Spring Boot pour la gestion des patients. Elle permet de créer, lire, mettre à jour et supprimer des informations sur les patients.

## Technologies Utilisées
- Java
- Spring Boot
- Maven
- Thymeleaf
- MySQL

## Configuration du Projet

### `pom.xml`
Le fichier `pom.xml` est utilisé par Maven pour gérer les dépendances et la configuration du projet.

### `application.properties`
Le fichier `application.properties` contient les configurations spécifiques à l'application Spring Boot.

## Structure du Projet

### Entités
- `Patient.java` : Représente un patient avec des attributs comme `id`, `nom`, `dateNaissance`, `malade`, et `score`.

### Référentiels
- `PatientRepository.java` : Interface pour gérer les entités `Patient`.

### Contrôleurs
- `PatientController.java` : Gère les requêtes web liées aux patients.
- `SecurityController.java` : Gère les requêtes web liées à la sécurité (login, non autorisé).

### Services
- `UserDetailsServiceImpl.java` : Implémente `UserDetailsService` pour charger les utilisateurs à partir de la base de données.

## Sécurité
Le projet utilise trois méthodes pour gérer les utilisateurs et les rôles :
1. `JdbcUserDetailsManager` (désactivée)
2. `InMemoryUserDetailsManager` (désactivée)
3. `UserDetailsServiceImpl` (activée)

## Templates Thymeleaf
- `template1.html` : Template de base.
- `patients.html` : Affiche la liste des patients.
- `formPatients.html` : Formulaire pour créer un nouveau patient.
- `editPatient.html` : Formulaire pour éditer un patient existant.
- `login.html` : Formulaire de connexion.
- `notAuthorized.html` : Page affichée lorsque l'utilisateur n'est pas autorisé.

