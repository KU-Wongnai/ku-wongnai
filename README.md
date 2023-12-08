# KU Wongnai

[Slide](https://www.canva.com/design/DAFyLdHz5nM/Ybhtk1yH4Sb0wa9ZQnzr1A/view?utm_content=DAFyLdHz5nM&utm_campaign=designshare&utm_medium=link&utm_source=editor)

## Setup

Clone this project with all other services

```sh
git clone --recurse-submodules https://github.com/KU-Wongnai/ku-wongnai.git
```

Create docker network

```sh
docker network create ku-wongnai_ku-wongnai
```

Run This command to start MySQL, Redis, Mailpit, RabbitMQ, PHPMyAdmin at the root of the project

```sh
docker-compose up -d
```

After that, you can go to each service and run

```sh
docker-compose up -d
```

to start the service located in `src` folder

## Performace Test

You can running the test with [JMeter](https://jmeter.apache.org/)

For the test to be passed you need to have this account in `user-service` database

Add this account to `user-service` database by making a POST request to `http://localhost:8090/register` with this body

```
{
    "name": "Weerawong Vonggatunyu",
    "email": "qu1etboy2@dev.io",
    "password": "12345678",
    "password_confirmation": "12345678"
}
```
