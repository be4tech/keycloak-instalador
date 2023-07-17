# 🔑 keycloak-heroku

---

> 一键部署 Keycloak 到 Heroku 平台。 Deploy Keycloak to Heroku by just one click.

[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=Jeff-Tian_keycloak-heroku&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=Jeff-Tian_keycloak-heroku)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=Jeff-Tian_keycloak-heroku&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=Jeff-Tian_keycloak-heroku)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=Jeff-Tian_keycloak-heroku&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=Jeff-Tian_keycloak-heroku)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=Jeff-Tian_keycloak-heroku&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=Jeff-Tian_keycloak-heroku)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=Jeff-Tian_keycloak-heroku&metric=bugs)](https://sonarcloud.io/summary/new_code?id=Jeff-Tian_keycloak-heroku)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=Jeff-Tian_keycloak-heroku&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=Jeff-Tian_keycloak-heroku)
[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=Jeff-Tian_keycloak-heroku&metric=duplicated_lines_density)](https://sonarcloud.io/summary/new_code?id=Jeff-Tian_keycloak-heroku)
[![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=Jeff-Tian_keycloak-heroku&metric=sqale_index)](https://sonarcloud.io/summary/new_code?id=Jeff-Tian_keycloak-heroku)


![https://api.star-history.com/svg?repos=jeff-tian/keycloak-heroku&type=Date](https://api.star-history.com/svg?repos=jeff-tian/keycloak-heroku&type=Date "Star History")


```shell
mvn clean install
docker compose up --build
```

运行部署到 heroku 的版本：

```shell
mvn clean install
docker compose -f docker-compose.heroku.yml up --build
```

在本地用 h2 数据库模拟部署到 heroku 的版本：

```shell
mvn clean install
docker compose -f docker-compose.local.yml up --build
open http://localhost:8080/
```


<a href="https://www.zhihu.com/consult/people/1073548674713423872" target="blank"><img src="https://first-go-vercel.vercel.app/api/dynamicimage" alt="向我咨询"/></a>

## 🇱🇷 English README

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

This repository deploys the [Keycloak](https://www.keycloak.org) Identity and Access Management Solution
to Heroku. It is based of Keycloak's official docker image with some slight modifications to use the
Heroku variable for `PORT` and `DATABASE_URL` properly.

The deployment will be made with a single Free dyno (although it won't run very well in smaller dynos
due to Java's memory hunger, it can be used as testing purpose without issues) with a free Postgres database attached.
