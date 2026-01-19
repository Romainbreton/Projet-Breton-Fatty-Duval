# Dictionnaire de citations littéraires interactif

## Description du projet

Le **Dictionnaire de citations littéraires interactif** est une application web permettant de consulter, ajouter et administrer des citations littéraires en ligne.  
Les données sont stockées dans une base de données MySQL et affichées dynamiquement via une interface web développée en PHP.

---

## Accès au site web

**Site officiel :**  
👉 https://citapedia.unaux.com

---

## Membres du projet

- Breton Romain  
- Fatty Dembo  
- Duval Ludovic  

---

## Fonctionnalités

### Fonctionnalités utilisateur
- Consultation libre des citations enregistrées
- Affichage dynamique des citations depuis la base de données

### Fonctionnalités administrateur
- Ajout de nouvelles citations via un formulaire sécurisé
- Suppression de citations existantes
- Gestion des droits selon le rôle utilisateur

### Sécurité et gestion
- Séparation des rôles utilisateur / administrateur
- Connexion sécurisée à la base de données MySQL
- Accès à la base via des comptes dédiés

---

## Technologies utilisées

- **Langages** : PHP, HTML, CSS  
- **Base de données** : MySQL  
- **Serveur** :  ProFreeHost 
- **Versioning** : GitHub  
- **Gestion de projet** : Trello  
- **Conception** : UML, MindView  
---

## Modélisation UML

La conception du système repose sur plusieurs diagrammes UML :
- Diagramme de cas d’utilisation (Utilisateur / Administrateur)
- Diagramme de classes
- Diagrammes de séquence pour :
  - l’ajout d’une citation  
  - la suppression d’une citation  

---

## Base de données

### Modèle relationnel

#### Table `citations`
- `id`
- `texte`
- `source_id`
- `created_by`
- `created_at`
- `updated_at`

#### Table `utilisateurs`
- `id`
- `nom_utilisateur`
- `mot_de_passe`
- `role`
- `created_at`
- `updated_at`

---

## Ajout de citations

L’ajout d’une citation s’effectue via un formulaire HTML relié à un script PHP qui :
- récupère les données saisies,
- établit une connexion à la base de données,
- exécute une requête SQL d’insertion,
- ferme la connexion MySQL.

---

## Affichage des citations

Les citations sont récupérées depuis la base de données à l’aide de requêtes SQL et affichées dynamiquement sur le site.

---

## Suppression des citations

La suppression est réservée aux administrateurs :
- sélection de la citation à supprimer,
- exécution de la requête SQL correspondante,
- mise à jour immédiate de l’affichage.

---

## Hébergement

- Hébergement du site sur ProFreeHost
- Base de données MySQL hébergée sur ProFreeHost

---

## Organisation du projet

- Code source versionné sur GitHub
- Suivi des tâches et de l’avancement via Trello
- Documentation et conception réalisées avec MindView et UML
