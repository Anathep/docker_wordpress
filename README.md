# docker_wordpress

This project runs a WordPress + MySQL stack using Docker Compose, with environment variables and secrets externalized for better security.

## Project Structure

- `compose.yml` — Defines services, volumes, secrets, and networks
- `.env` — Stores non-sensitive environment variables
- `docker/secrets/` — Secure directory for Docker secrets
- `README.md` — You're reading it!

## Environment Variables

These are defined in `.env`:

- `MYSQL_DATABASE`: name of the MySQL database (default: `wordpress`)
- `MYSQL_USER`: MySQL user (default: `wordpress`)
- `WORDPRESS_DB_HOST`: host used by WordPress to reach MySQL
- `WORDPRESS_DB_USER`: WordPress DB user
- `WORDPRESS_DB_NAME`: WordPress DB name

## Secrets

Secrets are used for sensitive values:

- `docker/secrets/mysql_root_password`: Root password for MySQL
- `docker/secrets/mysql_password`: User password for MySQL and WordPress
