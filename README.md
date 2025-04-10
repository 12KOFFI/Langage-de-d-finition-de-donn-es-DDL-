Projet de Base de Données : Gestion des Commandes Clients
Description du Projet
Ce projet implémente une base de données relationnelle pour gérer les clients, produits et commandes d'un système de vente. La structure comprend trois tables principales avec leurs relations et contraintes.

Schéma de la Base de Données
Tables Principales
Product (Produits)

Product_id (VARCHAR2(20)): Clé primaire

Product_Name (VARCHAR2(20)): Nom du produit (NOT NULL)

Price (NUMBER): Prix (doit être positif)

Catégorie (VARCHAR2(20)): Catégorie du produit (ajoutée ultérieurement)

Customer (Clients)

Customer_id (VARCHAR2(20)): Clé primaire

Customer_Name (VARCHAR2(20)): Nom du client (NOT NULL)

Customer_Tel (NUMBER): Téléphone du client

Orders (Commandes)

Customer_id (VARCHAR2(20)): Clé étrangère vers Customer

Product_id (VARCHAR2(20)): Clé étrangère vers Product

Quantity (NUMBER): Quantité commandée

Total_amount (NUMBER): Montant total

Date_commande (DATE): Date de commande (valeur par défaut SYSDATE)

Clé primaire composite: (Customer_id, Product_id)

Contraintes Implémentées
Clés primaires pour toutes les tables

Clés étrangères pour maintenir l'intégrité référentielle

Contraintes NOT NULL sur les champs critiques

Validation des données (Price > 0)

Valeur par défaut pour la date de commande
