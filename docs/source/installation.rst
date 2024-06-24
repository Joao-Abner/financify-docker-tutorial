=====================
Installation
=====================

1. **Clone the repository:**
  .. code-block:: bash
      git clone https://github.com/your-username/financify-docker-CRUD.git

2. **Navigate to the project directory:**
  .. code-block:: bash
      cd financify-docker-CRUD/financify/

3. **Build and start Docker containers:**
  .. code-block:: bash
      docker-compose up --build -d

4. **Access the PHP CRUD page in your browser:**
   - http://www.financify.com

5. **Verify containers status:**
  .. code-block:: bash
      docker-compose ps

6. **Remove all containers, volumes, and images:**
  .. code-block:: bash
      docker-compose down -v --rmi all

=====================
Deployment Guide
=====================

This section guides you through deploying your application using Docker and Docker Compose.

1. **Prerequisites**
   Ensure Docker and Docker Compose are installed.

2. **Repository Setup**
   - Clone the repository:
    .. code-block:: bash
        git clone https://github.com/your-username/financify-docker-CRUD.git
   - Navigate to the project directory:
    .. code-block:: bash
        cd financify-docker-CRUD/financify/

3. **Container Deployment**
   - Build and start containers:
    .. code-block:: bash
        docker-compose up --build -d

4. **Access Your Application**
   - Access via http://www.financify.com

5. **Monitor Container Status**
   - Check status:
    .. code-block:: bash
        docker-compose ps

6. **Clean Up**
   - Remove containers, volumes, and images:
    .. code-block:: bash
        docker-compose down -v --rmi all

For more details, see the relevant sections in this documentation.
