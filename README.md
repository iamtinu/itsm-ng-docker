# itsm-ng-docker

A Docker Compose configuration that sets up ITSM-NG with a PostgreSQL database, as described in the article https://wiki.itsm-ng.org/en/Installation/Docker.

How to use this docker-compose.yml file:
1) Save the content: Save the code above into a file named docker-compose.yml in an empty directory.
2) Open your terminal: Navigate to the directory where you saved the file.
3) Start the services: Run the command docker-compose up -d
-d runs the containers in detached mode (in the background).

Access ITSM-NG: Once the containers are up and running, you can access ITSM-NG in your web browser at http://localhost:1380.

Important Notes:

Passwords: The POSTGRES_PASSWORD and DB_PASSWORD are set to itsmng_password for simplicity. For any production environment, you must change this to a strong, unique password.
Ports: The application is exposed on port 8080 on your host machine. If this port is already in use, you can change 8080 to another available port (e.g., 9000:80).
Volumes: The db_data and app_data volumes ensure that your database and application files persist even if you stop or remove the containers.

This setup provides a robust and easy way to deploy ITSM-NG using Docker Compose
