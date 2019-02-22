# Cloudshack 

[![build status](https://api.travis-ci.org/diroussel/cloudshack.svg?branch=master)](https://dashboard.heroku.com/apps/cloudshack)

This application gets deployed to Heroku on every push to GitHub

## Based On

The basic setup for this project was provided by [http4k + Heroku + Travis](https://github.com/http4k/http4k-bootstrap)

## Getting Started

* Fork this repo
* Configure [Travis](https://travis-ci.org) to build the new repo
* Create your Heroku app:

```bash
heroku apps:create my-awesome-app
```

* Update the `app` entry in .travis.yml
* Update the deployment credentials

```bash
travis encrypt $(heroku auth:token) --add deploy.api_key
```

* Commit and push your changes to GitHub:

```bash
git commit -am"Update travis config"
git push origin master
```

This will automatically trigger a new build and deployment of your app.

## Running it locally

```bash
./gradlew stage
heroku local web
```

The app will be available on [http://localhost:5000](http://localhost:5000)

## Deploying it manually

```bash
git push heroku master
```
