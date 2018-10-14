# heroku-docker-deployment
Deploying Docker containers to Heroku

## Software (click for installation guide)
- [Docker](https://docs.docker.com/install/)
- [Docker-Compose](https://docs.docker.com/compose/)
- [Heroku](https://devcenter.heroku.com/)
- [Create-React-App](https://github.com/facebook/create-react-app)
- [Node.js](https://nodejs.org/en/)
- [Express](https://expressjs.com/)
- [Postgres](https://www.postgresql.org/)
- [Redis(?)](https://redis.io/)

## Guide
### Set Up Local Development Environment

1. Create a `.env` using `.example.env` as an example. 
1. In `docker-compose.yml` change the value of the `image` property to match the `IMAGE_NAME` value of `.env`
1. Run `docker-compose build` to build the services images
1. Run `docker-compose up -d` to run the container in the background

__If no errors__
1. Run `docker-compose down` to stop the container from running in the background

### Deploy to Heroku
1. `heroku container:login`
1. Navigate to project directory
1. `heroku create`
1. `heroku container push web`
1. `heroku container release web`
1. `heroku open`

## Troubleshooting


## Sources
[Local Development with Docker Compose](https://devcenter.heroku.com/articles/local-development-with-docker-compose)
[Docker Deploys with Heroku](https://devcenter.heroku.com/articles/container-registry-and-runtime)


