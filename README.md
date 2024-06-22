# Laravel Docker Environment

This repository provides a Docker setup for running a Laravel application.

## Getting Started

Follow these instructions to get your Laravel application up and running with Docker.

### Prerequisites

Make sure you have Docker and Docker Compose installed on your machine.

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Setup

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/teknik-github/laravel-docker.git
   cd laravel-docker
   ```

2. **Add Your Laravel Application**:

   Copy your Laravel application into the `web` folder of the repository.

3. **Start Docker Containers**:

   Run the following command to start the Docker containers:

   ```sh
   docker-compose up -d
   ```

   Wait for about 30 seconds to 1 minute, depending on your device's performance.

4. **Access the Application**:

   Open your web browser and go to [http://localhost:8000](http://localhost:8000) or use your IP address [http://ip:8000](http://ip:8000).

### Folder Structure

- `web`: This folder should contain your Laravel application.

### Docker Services

- **MariaDB**: Database service for Laravel.
- **Laravel**: The Laravel application service.

### Docker Volumes

- `mariadb_data`: Persistent storage for MariaDB data.

### Environment Variables

The Docker Compose file sets the following environment variables for the Laravel service:

- `DB_HOST=mariadb`
- `DB_PORT=3306`
- `DB_USERNAME=bn_myapp`
- `DB_DATABASE=bitnami_myapp`

You can customize these variables in the `docker-compose.yml` file if needed.

### Troubleshooting

If you encounter any issues, check the logs of the Docker containers:

```sh
docker-compose logs -f
```

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request with your improvements.
