Welcome to Financify-docker's documentation!

.. toctree::
:maxdepth: 2
:caption: Contents:
introduction
installation
usage
deployment
.. Read the Docs documentation: https://financify-docker-tutorial.readthedocs.io/en/latest/
Introduction
Financify-Docker-CRUD is a PHP-based web application that demonstrates CRUD (Create, Read, Update, Delete) operations using a MySQL database, all packaged within a Docker container environment. This project is an example implementation of a simple financial management system, inspired by the Udarax.me tutorial.
The main objective of this application is to provide a practical example of how to build a web application with a PHP backend, MySQL database, and containerize the entire stack using Docker. This project can serve as a starting point for developers who want to learn about building and deploying web applications with PHP, MySQL, and Docker.
Key features of the Financify-Docker-CRUD application include:
CRUD Operations: Users can create, read, update, and delete financial records stored in a MySQL database.
Docker Containerization: The entire application stack, including PHP and MySQL, is packaged and deployed using Docker containers.
By exploring the Financify-Docker-CRUD project, developers can learn about the following concepts and technologies:
PHP Programming: Understand the fundamentals of PHP and how to build a web application with it.
MySQL Database Integration: Learn how to integrate a MySQL database with a PHP application and perform CRUD operations.
Docker Containerization: Explore the benefits of containerizing a web application and its components using Docker.
This project is designed to be a learning resource for developers who want to enhance their skills in web application development, database integration, and containerization using Docker.
Installation
Step-by-Step Installation Guide
Clone the repository:
bash
git clone https://github.com/your-username/financify-docker-CRUD.git

Navigate to the project directory:
bash
cd financify-docker-run/financify/

Build and start the Docker container:
bash
docker-compose up --build -d

Open the PHP CRUD page in your browser:
bash
http://www.financify.com

Verification and Removal
Verify:
bash
docker compose ps

Remove:
bash
docker compose down -v --rmi all

Usage
Using the Application
Creating a New Record
Open a web browser and navigate to http://localhost:8080.
Click on the "Create" button to open the form for creating a new record.
Fill in the required fields with the necessary information.
Click the "Submit" button to create the new record.
Reading a Record
Open a web browser and navigate to http://localhost:8080.
Click on the "Read" button to view the list of existing records.
Select a record from the list to view its details.
Updating a Record
Open a web browser and navigate to http://localhost:8080.
Click on the "Update" button to open the form for updating an existing record.
Select the record to update from the list.
Fill in the required fields with the necessary information.
Click the "Submit" button to update the record.
Deleting a Record
Open a web browser and navigate to http://localhost:8080.
Click on the "Delete" button to delete an existing record.
Select the record to delete from the list.
Confirm the deletion by clicking the "Yes" button.
Deployment
Deployment Process
This section covers the deployment process for your application.
