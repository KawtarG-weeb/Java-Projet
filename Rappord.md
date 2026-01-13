# Kawtar GOUY           
# 4IIR G2
# Titre du projet: Online Shopping
<img width="724" height="700" alt="12-class-diagram-online-shopping" src="https://github.com/user-attachments/assets/bc59ea05-0443-4af8-b02a-d1947ef9e771" />

# Rapport de Projet  
## ProductShopping

## 1. Présentation du projet
ProductShopping est une application desktop développée en Java.  
Elle permet de gérer et consulter des produits, puis de simuler un parcours d’achat.  
L’application utilise JavaFX pour l’interface graphique et Hibernate pour la persistance des données dans une base MySQL.

## 2. Objectifs
- Afficher un catalogue de produits clair et structuré  
- Permettre la gestion des produits côté administration  
- Assurer un stockage fiable des données  
- Séparer l’interface, la logique métier et l’accès aux données  

## 3. Fonctionnalités

### 3.1 Côté utilisateur
- Affichage de la liste des produits  
- Consultation des détails d’un produit  
- Recherche par nom  
- Filtrage par catégorie  
- Ajout de produits au panier  
- Mise à jour des quantités  
- Calcul automatique du total  
- Validation de commande selon l’implémentation  

### 3.2 Côté administration
- Ajouter un produit  
- Modifier un produit  
- Supprimer un produit  
- Gérer les catégories si disponibles  
- Valider les champs avant l’enregistrement  

## 4. Architecture technique

### 4.1 Architecture MVC
- Model  
  - Entités JPA représentant les tables MySQL  
- DAO / Repository  
  - Méthodes CRUD  
  - Utilisation de Hibernate Session et Transaction  
- Service  
  - Logique métier  
- Controller  
  - Gestion des actions utilisateur  
  - Interaction entre vue et services  
- View  
  - Interfaces JavaFX et fichiers FXML  

### 4.2 Persistance des données
- Configuration Hibernate dans les ressources  
- Mapping par annotations JPA  
- Gestion des transactions pour garantir la cohérence  

## 5. Technologies utilisées

### 5.1 Langage et outils
- Java 21  
- Maven  

### 5.2 Interface graphique
- JavaFX  
- ControlsFX  
- FormsFX  
- ValidatorFX  
- Ikonli  
- BootstrapFX  

### 5.3 Base de données
- MySQL  
- MySQL Connector/J  
- Hibernate ORM  
- Jakarta Persistence API  

## 6. Exécution du projet

### 6.1 Prérequis
- JDK 21 installé  
- MySQL opérationnel  
- Base de données configurée  
- Paramètres corrects dans Hibernate  

### 6.2 Lancement
Commande Maven 

## 7. Modèle de données

Exemple de classes :
- Product  
- Category  
- CartItem  
- Order  
- OrderLine  

Relations principales :
- Une catégorie possède plusieurs produits  
- Une commande contient plusieurs lignes de commande  
- Un produit peut apparaître dans plusieurs commandes  

## 8. Difficultés rencontrées et solutions

### Problème 1 : Configuration JavaFX avec Maven
Solution :  
- Ajout du plugin JavaFX Maven  
- Vérification de la classe principale  

### Problème 2 : Connexion MySQL avec Hibernate
Solution :  
- Vérification des paramètres de connexion  
- Chargement correct du driver MySQL  

### Problème 3 : Gestion des transactions
Solution :  
- Utilisation systématique de begin et commit  
- Gestion des erreurs avec rollback  

### Problème 4 : Validation des champs
Solution :  
- Vérification des entrées utilisateur  
- Affichage de messages d’erreur clairs  

## 9. Conclusion et perspectives
Le projet ProductShopping combine une interface JavaFX moderne et une persistance robuste avec Hibernate.  
Il respecte une architecture claire et facilite la maintenance.

Améliorations possibles :
- Authentification des utilisateurs  
- Gestion avancée du stock  
- Historique des commandes  
- Génération de factures  
- Upload et gestion des images produits  

