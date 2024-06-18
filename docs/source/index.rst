Welcome to Financify-Docker's Documentation!
============================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   introduction
   installation
   usage
   deployment

.. Read the Docs documentation: https://financify-docker-tutorial.readthedocs.io/en/latest/


Introduction
------------

Financify-Docker-CRUD is a PHP-based web application that demonstrates CRUD (Create, Read, Update, Delete) operations using a MySQL database, all packaged within a Docker container environment. This project serves as a practical example of building and deploying a web application with PHP, MySQL, and Docker. Inspired by the Udarax.me tutorial.

Key Features
~~~~~~~~~~~~

- **CRUD Operations:** Perform Create, Read, Update, and Delete operations on financial records in MySQL.
- **Docker Containerization:** Entire stack (PHP, MySQL) is containerized for seamless deployment.

This project is designed for developers looking to:
- Understand PHP fundamentals for web development.
- Integrate MySQL databases with PHP applications.
- Utilize Docker for containerized deployment.

Installation
------------

1. **Clone the repository:**

   ::

       git clone https://github.com/your-username/financify-docker-CRUD.git

2. **Navigate to the project directory:**

   ::

       cd financify-docker-CRUD/financify/

3. **Build and start Docker containers:**

   ::

       docker-compose up --build -d

4. **Access the PHP CRUD page in your browser:**

   - [http://www.financify.com](http://www.financify.com)

Verify containers status:

   ::

       docker-compose ps

To remove all containers, volumes, and images:

   ::

       docker-compose down -v --rmi all

Usage
-----

This section explains how to interact with your application:

Creating a New Record
~~~~~~~~~~~~~~~~~~~~~

1. Open a web browser and navigate to [http://localhost:8080](http://localhost:8080).
2. Click the "Create" button to open the new record form.
3. Fill in the required fields.
4. Click "Submit" to create the record.

Reading a Record
~~~~~~~~~~~~~~~~

1. Navigate to [http://localhost:8080](http://localhost:8080).
2. Click the "Read" button to view existing records.
3. Select a record to view details.

Updating a Record
~~~~~~~~~~~~~~~~~

1. Navigate to [http://localhost:8080](http://localhost:8080).
2. Click the "Update" button to modify a record.
3. Select the record and update details.
4. Click "Submit" to save changes.

Deleting a Record
~~~~~~~~~~~~~~~~~

1. Navigate to [http://localhost:8080](http://localhost:8080).
2. Click the "Delete" button to remove a record.
3. Confirm deletion by clicking "Yes".

Deployment
----------

This section covers deploying your application:

- Ensure Docker and `docker-compose` are installed.
- Clone the repository, navigate to the project directory.
- Use `docker-compose` to build and start containers.
- Access your application through the provided URL.

For detailed steps and examples, refer to the respective sections above.

