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
```text
Fournil.App/
├── Models/
│   └── Produit.cs          # Product entity and display formatting
├── Services/
│   ├── Catalogue.cs        # ID generation and product lookup logic
│   ├── Saisie.cs           # Console input parsing and validation
│   └── StockageJson.cs     # JSON serialization and file persistence
├── Program.cs              # Main CLI menu loop
└── Fournil.App.csproj      # .NET 10.0 project configuration
