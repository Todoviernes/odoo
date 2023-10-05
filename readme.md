
# Odoo Docker

This project provides a Docker Compose setup to deploy Odoo 16.0 with a PostgreSQL 15 backend. It uses Docker secrets to manage the PostgreSQL password securely.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Setup & Deployment

1. **Clone the Repository**

    ```bash
    git clone [your-repo-url] my-odoo-project
    cd my-odoo-project
    ```

    Replace `[your-repo-url]` with the URL of your Git repository.

2. **Set Up the PostgreSQL Password**

    First, you need to set a secure password for the PostgreSQL database:

    ```bash
    echo "your_secure_password" > odoo_pg_pass
    ```

    Remember to replace `your_secure_password` with a strong, secure password.

3. **Run the Project**

    Now, you can start the project using Docker Compose:

    ```bash
    docker-compose up -d
    ```

    This will pull the necessary Docker images and start the Odoo and PostgreSQL services.

4. **Access Odoo**

    Once the services are running, you can access the Odoo instance by navigating to:

    ```
    http://localhost:8069
    ```

## Custom Addons

If you have custom or additional modules/addons for Odoo, place them in the `addons/` directory. Each module should have its own sub-directory containing its files and assets.

## Configuration

- Odoo configurations can be adjusted in the `config/` directory, specifically within the `odoo.conf` file if you have one.
  
- The PostgreSQL password is managed as a Docker secret, sourced from the `odoo_pg_pass` file.

## Clean Up

To stop the services and remove the containers, you can use:

```bash
docker-compose down
```

## Feedback & Contributions

Feel free to raise issues or provide feedback. Contributions to this project are welcome!

---

You can adjust the content above as needed, such as adding more specific details, badges, or other relevant sections to fit the specific needs of your project.