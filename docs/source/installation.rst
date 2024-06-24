=====================
 Installation
=====================

1.  **Clone the repository:**

        git clone https://github.com/your-username/financify-docker-CRUD.git

2.  **Navigate to the project directory:**

        cd financify-docker-CRUD/financify/

3.  **Build and start Docker containers:**

        docker-compose up --build -d

4.  **Access the PHP CRUD page in your browser:**

    - [http://www.financify.com](http://www.financify.com)

Verify containers status:

       docker-compose ps

To remove all containers, volumes, and images:

       docker-compose down -v --rmi all

=====================
Deployment Guide
=====================

This section outlines the process for deploying your application using Docker and Docker Compose.

1. **Prerequisites**
   Ensure you have Docker and Docker Compose installed on your system. These tools are essential for building and managing the application's containers.

2. **Repository Setup**
   - Clone the application repository to your local machine using Git:

git clone https://github.com/your-username/financify-docker-CRUD.git


- Navigate to the project directory within the cloned repository:

cd financify-docker-CRUD/financify/


3. **Container Deployment**
   - Build and start the Docker containers defined in the project using Docker Compose:

docker-compose up --build -d


     This command builds the images if they don't exist and starts the containers in detached mode.

4. **Accessing Your Application**
   - Once the containers are up and running, access your application by navigating to the provided URL in your web browser. For example:

     - http://www.financify.com

5. **Monitoring Container Status**
   - To verify the status of the running containers, execute:

docker-compose ps


6. **Cleaning Up**
   - When you're done testing or need to redeploy, you can stop and remove the containers, networks, and images created by the project with:

docker-compose down -v --rmi all


For a comprehensive walkthrough and additional examples, please consult the relevant sections earlier in this documentation.
