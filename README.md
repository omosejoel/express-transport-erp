# Express Transport Limited – Odoo 19 ERP

## Project Overview

Express Transport Limited is a transport management ERP system developed using Odoo 19. The system is designed to help manage transport business operations, including vehicles, employees, sales, customers, and other business records.

The ERP was initially developed and tested locally and was later deployed to the cloud as part of the "From Local Host to Global Cloud" deployment assignment.

## Technologies Used

- Odoo 19
- PostgreSQL
- Railway Cloud Platform
- Python
- GitHub

## Cloud Provider

### Railway

Railway was selected as the cloud deployment platform for this project because it provides a simple deployment environment for web applications and databases and allows the ERP to be accessed through a public URL.

## Database

The ERP uses PostgreSQL as its database.

The database is hosted separately through the cloud deployment environment and connected to Odoo using environment variables.

No database passwords or sensitive credentials are stored directly in the source code.

## Live ERP

Live URL:

https://odoo-production-21b7.up.railway.app/

The deployed ERP can be accessed through the public Railway URL.

## Deployment Process

### 1. Prepare the ERP

The Odoo 19 ERP was first configured and tested locally. The required modules, users, business records, and database were prepared before deployment.

### 2. Create the Cloud Project

A Railway project was created for the Odoo ERP deployment.

### 3. Configure PostgreSQL

A PostgreSQL database was created and connected to the Odoo application.

### 4. Configure Environment Variables

The database connection information was configured using environment variables instead of hardcoding database credentials.

Examples of environment variables include:

- PGHOST
- PGPORT
- PGUSER
- PGPASSWORD
- PGDATABASE

Sensitive values such as passwords are not included in this repository.

### 5. Deploy Odoo

The Odoo 19 application was deployed to Railway using the Odoo 19 container image.

### 6. Configure the Database

Odoo was connected to the PostgreSQL database and the required ERP database was initialized.

### 7. Test the Deployment

After deployment, the ERP was accessed through the public Railway URL.

The following were tested:

- User login
- Sales access
- Fleet access
- Record creation
- Record viewing
- Record editing
- Assessor account access

## Test Records

Three sample sales records were created to demonstrate that the deployed ERP was working correctly.

The records were also checked using the assessor account.

## Assessor Account

An assessor account was created for assessment purposes.

Username:

assessor@swone.com

The password is intentionally not stored in this public GitHub repository. It is provided separately through the official assessment submission.

## Access Rights

The assessor account was given the required permissions to test the ERP, including access to:

- Sales
- Fleet
- Inventory
- Invoicing
- Other required ERP functions

## Challenges Encountered

### Challenge 1 – Database Connection

During deployment, there were PostgreSQL connection problems. The application initially could not correctly resolve the database host.

This was resolved by checking the PostgreSQL configuration and ensuring that the correct database connection variables were supplied to the cloud application.

### Challenge 2 – Odoo Database Initialization

An Odoo database initialization problem occurred during deployment, resulting in an error related to the Odoo HTTP model.

The database configuration was reviewed and the Odoo database was properly initialized before testing the application again.

## Testing Results

The deployed ERP was successfully tested by:

1. Logging into the public Odoo system.
2. Creating an assessor account.
3. Creating three sample sales records.
4. Logging in using the assessor account.
5. Confirming that the assessor could view the records.
6. Testing record interaction.

## Project Purpose

This project demonstrates the migration of an ERP system from a local development environment to a publicly accessible cloud environment.

It also demonstrates practical skills in:

- Cloud deployment
- ERP configuration
- Database management
- User access control
- PostgreSQL
- Troubleshooting
- Version control using GitHub

## Author

Express Transport Limited ERP Project

Information Systems and Technology (IST)
Southern Delta University
