# Sakila Project - ASP.NET Core MVC with Identity

This project is an MVC web application that integrates ASP.NET Core Identity, Google OAuth authentication, email confirmation (Gmail SMTP), and PostgreSQL storage. It meets all the requirements for security integration and role management.

## Technologies Used
* ASP.NET Core MVC (.NET 8/10)
* Entity Framework Core
* PostgreSQL
* ASP.NET Core Identity
* Google Cloud Console (OAuth)
* MailKit (SMTP)

## Execution Instructions

To run this project in your local environment, follow these steps:

### 1. Clone the repository
Clone the repository to your local machine:
```bash
git clone https://github.com/Sahid-B/oAuth-and-Multifactor-in-.NET_Sahid-Bosquez-.git
```

### 2. Restore the database
The project uses PostgreSQL. You must restore the database to have all the identity tables and test information:
* Open pgAdmin or your PostgreSQL manager.
* Create an empty database named `sakila`.
* Restore the backup file located in the `BackupdeSakila` folder included in this repository.

### 3. Configure Credentials (optional)
The `appsettings.json` file already includes the PostgreSQL connection string. If your local Postgres credentials are different (Username/Password), change them in the `ConnectionStrings` section:
```json
"DefaultConnection": "Host=localhost;Port=5432;Database=sakila;Username=YOUR_USERNAME;Password=YOUR_PASSWORD"
```
*(Note: Google keys and the test email password are included in the file for academic functionality demonstration purposes, while `client_secret` files are git-ignored for safety).*

### 4. Run the application
Open a terminal in the project root folder (`SakilaApp`) and execute the following commands:
```bash
dotnet restore
dotnet run
```
The application will normally start on `http://localhost:5055` or the configured port.

### 5. Test Users (Credentials)
Once the application is running, you can use the following default seed users to test the system's roles and restrictions:

* **Administrator:** 
  * Email: `admin@espe.edu.ec` 
  * Password: `Admin123*`
* **Employee:** 
  * Email: `empleado@espe.edu.ec` 
  * Password: `Admin123*`

## Screenshots (Evidences)
All screenshots required by the rubric (Google Cloud Configurations, PostgreSQL Tables, Login, 2FA, Access Denied, etc.) are attached in the `Evidencias_Fotos` folder of this repository.
