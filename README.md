# 🔑 keycloak-heroku

## README

## Hacer el deploy de Keycloak version 19.0.1 en Heroku. Carga el tema personalizado y algunas utilidades adicionales.

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

This repository deploys the [Keycloak](https://www.keycloak.org) Identity and Access Management Solution
to Heroku. It is based of Keycloak's official docker image with some slight modifications to use the
Heroku variable for `PORT` and `DATABASE_URL` properly.

The deployment will be made with a single Free dyno (although it won't run very well in smaller dynos
due to Java's memory hunger, it can be used as testing purpose without issues) with a free Postgres database attached.
