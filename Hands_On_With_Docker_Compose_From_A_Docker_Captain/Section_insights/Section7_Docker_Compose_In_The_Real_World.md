## Section Insights

**Worth Learning Docker**

- Yes it is worth because docker  is an open source containerization platform it enables developers to package software application into containers—standardized.

**Adding Docker Compose**

- A tool called Docker Compose was created to make it easier to define and share multi-container applications.
```
version: '3'

services:
  redis:
    image: 'redis:3.2-alpine'
    ports:
      - '6379:6379'
    volumes:
      - 'redis:/data'

  web:
    build: .
    depends_on:
      - 'redis'
    env_file:
      - '.env'
    ports:
      - '5000:5000'
    volumes:
      - '.:/app'

volumes:
  redis: {}
```

- `$docker-compose build` Will build services.

- `$docker-compose pull` Pulling an service image. 

- `$docker-compose up` Creating and start a containers.

- `$docker-compose up --build -d` -shortcut for launching containers in the background with build pull and up -d

- `$docker-compose ps` - this is the list of containers.

- `$docker-compose restar`t` - Restart a containers.

- `$docker-compose stop` - Stopping a services




