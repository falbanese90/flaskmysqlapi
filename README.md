# One stop Shop Flask API User Login Authentication & MySQL DB with Docker

## Requirements

- Docker Desktop: Make sure you have Docker Desktop installed and running on your machine.

## Setup Instructions

1. Change to the project's root directory:

   ```bash
   cd project-directory
   ```

2.  Run the following command to start the Docker container cluster

    ```bash
    docker-compose -f 'docker-compose.yml' up -d
    ```
    This command will pull the required Docker images and start the containers defined in the Docker Compose file.

3. Once the container cluster is running, you can access the following endpoints:

    - Register User: http://localhost:5000/register
    - Login User: http://localhost:5000/login

    ```json
    {
    "username": "<yourusername>",
    "password": "<yourpassword>"
    }
    ```
    Replace <yourusername> and <yourpassword> with your desired values.

On a successful login it will return a payload containing Success message and a JWT. Example below:
```json
    {
    "message": "Login successful",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.                     eyJ1c2VybmFtZSI6ImZhbGJhbmVzZTkwIiwiZXhwIjoxNjg2MDg1NTA4fQ.WUk_Hx2K53LbOgHqeArIH9lGWGNx8LC2HsHCf5_RqMs"
    }
```