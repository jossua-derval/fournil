[English](#fournil--bakery-catalog--stock-management) | [Français](#fournil--gestion-de-catalogue-et-de-stock-de-boulangerie)

---

## Fournil — Bakery Catalog & Stock Management

A C# / .NET console application designed to manage a bakery's product catalog and inventory. Built as an evolving hands-on project to apply Object-Oriented Programming (OOP), clean code separation, and input validation practices.

*(Note: The application's domain model and console interface are in French.)*

### Current Features
* **Catalog Display:** Lists available products across three categories (`Pain`, `Viennoiserie`, `Pâtisserie`) with pricing and current stock levels.
* **Product Creation:** Adds new items with automatic ID generation and strict user input validation (non-empty strings, positive decimal prices, valid category selection).
* **Stock Management:** Looks up products by ID and updates inventory quantities safely.
* **JSON Persistence:** Automatically loads and saves catalog changes to a local `produits.json` file.

### Project Structure

    Fournil.App/
    ├── Models/
    │   └── Produit.cs          # Product entity and display formatting
    ├── Services/
    │   ├── Catalogue.cs        # ID generation and product lookup logic
    │   ├── Saisie.cs           # Console input parsing and validation
    │   └── StockageJson.cs     # JSON serialization and file persistence
    ├── Program.cs              # Main CLI menu loop
    └── Fournil.App.csproj      # .NET 10.0 project configuration

### Getting Started
* **Prerequisite:** [.NET 10.0 SDK](https://dotnet.microsoft.com/download)

    git clone [https://github.com/jossua-derval/fournil.git](https://github.com/jossua-derval/fournil.git)
    cd fournil/Fournil.App
    dotnet run

### Roadmap (Upcoming Improvements)
* [ ] Migrate data persistence from JSON to **SQL Server** using **Entity Framework Core**
* [ ] Expose business logic through an **ASP.NET Core REST API**
* [ ] Add unit tests (xUnit) for catalog and validation services
* [ ] Containerize the application with **Docker**

---

## Fournil — Gestion de catalogue et de stock de boulangerie

Application console en C# / .NET conçue pour gérer le catalogue de produits et les stocks d'une boulangerie. Développée comme projet fil rouge évolutif pour mettre en pratique la Programmation Orientée Objet (POO), la séparation des responsabilités et la validation des entrées utilisateur.

### Fonctionnalités actuelles
* **Affichage du catalogue :** Liste les produits disponibles selon trois catégories (`Pain`, `Viennoiserie`, `Pâtisserie`) avec leur prix et leur niveau de stock.
* **Ajout de produits :** Création de nouveaux articles avec génération automatique d'identifiant et contrôle strict des saisies (chaînes non vides, prix décimal positif, sélection dans une liste autorisée).
* **Gestion des stocks :** Recherche d'un produit par son identifiant et mise à jour sécurisée des quantités.
* **Persistance JSON :** Chargement et sauvegarde automatiques des modifications dans un fichier local `produits.json`.

### Structure du projet

    Fournil.App/
    ├── Models/
    │   └── Produit.cs          # Entité produit et formatage de l'affichage
    ├── Services/
    │   ├── Catalogue.cs        # Génération d'ID et recherche dans le catalogue
    │   ├── Saisie.cs           # Lecture et validation des entrées console
    │   └── StockageJson.cs     # Sérialisation JSON et persistance sur fichier
    ├── Program.cs              # Boucle principale du menu CLI
    └── Fournil.App.csproj      # Configuration du projet .NET 10.0

### Installation et exécution
* **Prérequis :** [.NET 10.0 SDK](https://dotnet.microsoft.com/download)

    git clone [https://github.com/jossua-derval/fournil.git](https://github.com/jossua-derval/fournil.git)
    cd fournil/Fournil.App
    dotnet run

### Évolutions prévues
* [ ] Migrer la persistance des données de JSON vers **SQL Server** avec **Entity Framework Core**
* [ ] Exposer la logique métier via une **API REST ASP.NET Core**
* [ ] Ajouter des tests unitaires (xUnit) pour les services de catalogue et de saisie
* [ ] Conteneuriser l'application avec **Docker**
