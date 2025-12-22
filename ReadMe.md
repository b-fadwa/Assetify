# 🖥️ Assetify Application

This demo app is built with **4D Qodly Pro** and is meant to inspire you or help you kickstart your own IT asset management project.

## Purpose

The **Assetify Application** centralizes IT operations into a single, intuitive system.  
It helps teams manage IT assets, software licenses, incidents, and users while ensuring clear role-based access for staff.

## Main Features

- **Dashboard**: Global overview of assets, licenses, incidents, and upcoming expirations.  

![Dashboard page](Project/Sources/Shared/assets/images/dash.png)
- **Asset Management**: Track all IT equipment with details such as type, status, location, and assigned user.  

![Equipments page](Project/Sources/Shared/assets/images/equipments.png)
- **Software & License Management**: Monitor software installations, license validity, and compliance. 

![Software page](Project/Sources/Shared/assets/images/softwares.png)
- **Incident Management**: Create, assign, and resolve IT incidents with tracking and notifications.  

![Incidents page](Project/Sources/Shared/assets/images/incidents.png)
- **License Expiration Calendar**: Visual overview of upcoming renewals and expirations. 

![Licenses page](Project/Sources/Shared/assets/images/licenses.png)
- **User Management**: Manage users, roles, and access permissions.

![Users page](Project/Sources/Shared/assets/images/users.png)
- **Settings**: Configure system-wide settings and preferences.

![Settings page](Project/Sources/Shared/assets/images/settings.png)


## How to Run

### Pre-requisites (4D Software)
- Download the latest Release version of 4D: [Product Download](https://us.4d.com/product-download/Feature-Release)  
- Or the latest Beta version: [Beta Program](https://discuss.4d.com/)  
- Follow activation steps: [Installation Guide](https://developer.4d.com/docs/GettingStarted/installation)

### Steps to Run the Project
- Clone or download this repository to your local machine.  
- Open the project in 4D: **File > Open Project**  
- Open **Qodly Studio**: **Design > Qodly Studio**  
- Click **Run** to start the server and preview the app in your browser.

## Configuration & Credentials

### Do I need to create external accounts?
- **Mailing (optional)**: Required only if you want email notifications (incident updates, alerts).  
  Assetify supports sending emails via **SMTP-compatible services** such as **SendGrid SMTP**.

### Where does the app read credentials?
- Credentials are inputted in the Setting page in the application.


## Test Accounts and Sample Data  
- Sample data can be generated via a dedicated data generator method or from the UI.

## Where to Find the Code for Each Feature

- **Authentication & Roles**
  - Server: `DataStore.4dm` (authentication & session privileges)  
  - UI: `login.WebForm` / `index.WebForm`

- **Dashboard**
  - UI: `dashboard.WebForm`  
  - Server/Data: `Type.4dm`,`status.4dm`,`IncidentHistory.4dm`,`Type.4dm`,`Datastore.4dm`..

- **Asset Management**
  - UI: `equipmentInventory.WebForm`,,`equipmentInventory.WebForm`  
  - Server/Data: `Equipment.4dm`, `EquipmentEntity.4dm`, `UserEquipmentEntity.4dm`

- **Software & License Management**
  - UI: `softwareInventory.WebForm`  
  - Server/Data: `EquipmentSoftware.4dm`, `License.4dm`

- **Incident Management**
  - UI: `incidentHistory.WebForm`  
  - Server/Data: `IncidentHistory.4dm`, `IncidentHistoryEntity.4dm`

- **License Expiration Calendar**
  - UI: `licenseInventory.WebForm`,`calendar.webform` 
  - Server/Data: `License.4dm`, `LicenseEntity.4dm`

- **User Management**
  - UI: `userManagement.WebForm`  
  - Server/Data: `User.4dm`, `Role.4dm`

- **Settings**
  - UI: `settings.WebForm`  

This structure allows you to easily customize, extend, or reuse the Assetify application as a foundation for your own IT operations solutions.
