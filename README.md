# fastapi-celery-flower-rabbitmq-redis

This repository serves as an illustrative example of implementing FastAPI with Celery within Docker containers. The underlying architecture involves Celery utilizing RabbitMQ as the message broker and Redis as the backend.

The example demonstrates a simulation where fictitious emails are sent through a FastAPI-powered REST API. The email sending process, though simulated, may take between 1 to 4 seconds. Thanks to the asynchronous queue management of Celery, the application remains unblocked throughout this process.

## Requirements

To successfully run and understand this example, ensure you have the following components installed:

- **Git**
- **Docker Compose** (version 19.03.0+)

## Running

Follow these steps to run the example on your local machine:

1. Clone the repository:

```sh
git clone https://github.com/luovkle/fastapi-celery-flower-rabbitmq-redis.git
cd fastapi-celery-flower-rabbitmq-redis
```

2. Build and start the Docker containers using Docker Compose:

```sh
docker compose up -d
```

3. Wait for the containers to be up and running. The FastAPI application, Celery workers, RabbitMQ, and Redis services should all be active.

## Accessing Services

Once the containers are up, you can access the following services:

- **FastAPI** REST API: Access the FastAPI application by navigating to **http://localhost:8000** in your web browser or using tools like curl or Postman.
- **Flower** Monitoring Dashboard: Monitor the Celery tasks and workers by visiting **http://localhost:5555** in your web browser.
- **RabbitMQ** Management UI: Observe the message broker's activity at **http://localhost:15672**. The default login credentials are **guest** for both username and password.
- **Redis**: Redis, used as the backend, is internally accessible to the containers within the network.

Feel free to explore the code in this repository to gain a better understanding of how FastAPI, Celery, RabbitMQ, and Redis are integrated to create an asynchronous email processing system.

For any issues or inquiries, please open an issue on this repository.

## Note

This example is intended for educational purposes and might not reflect a production-ready setup. Make sure to adapt it according to your needs and security considerations before deploying it in a production environment.
