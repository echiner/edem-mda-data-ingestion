# EDEM - Master on Data Analytics - Data Ingestion

## Introduction

<img width="250" src="https://nifi.apache.org/assets/images/apache-nifi-logo.svg">

In these section we will setup **[Apache NiFi](https://nifi.apache.org/)** and ingest data from various sources into Hadoop.

## Initial Setup

We will be using the Docker Compose in this root folder, so start the Docker Compose components:

```shell
docker-compose up -d
```

```shell
# List the running services
docker ps

# Stop a specific service
docker-compose stop <SERVICE>
```

## Services

You will find the services in the following URLs:

* [Apache NiFi](https://localhost:8443/nifi)
  * **Username**: admin
  * **Password**: ctsBtRBKHRAx69EqUghvvgEvjnaLjFEB
* [NiFi Registry](http://localhost:18080/nifi-registry)

## Exercises

* [**Exercise 1**: Building our first Data Flow - File to File](Exercises/Exercise1)
* [**Exercise 2**: Basic Ingestion (I) - HTTP to File](Exercises/Exercise2)
* [**Exercise 3**: Basic Ingestion (II) - HTTP to File, with data manipulation](Exercises/Exercise3)
* [**Exercise 4**: Complex Data Ingestion - Real-time Flights](Exercises/Exercise4)
* [**Exercise 5**: GDELT Data Ingestion ](Exercises/Exercise5)
* [**Exercise 6**: Ingesting real-time data](Exercises/Exercise6)

## Understanding the components

Given that we will be reusing the same Docker Compose that we used in previous courses, we will have the same components (NameNode, DataNode, etc.), but in our case we will focus on the following:

* **Apache NiFi**: Ingestion tool used in the course
* **Apache NiFi Registry**: Code management and repository for Apache NiFi
* **MongoDB**: NOSQL document database for storing JSON
* **MongoDB Express**: Basic MongDB front-end for viewing and searching data

Here is the list of components and ports:

| Component  | Docker Service | Port |
| ------------- | ------------- | ------------- |
| Apache NiFi  | nifi  |  [8443](https://localhost:8443/nifi) |
| Apache NiFi Registry   | nifi-registry  | [18080](http://localhost:18080/nifi-registry)  |
| MongoDB   | mongo  | 27017  |
| MongoDB Express - UI   | mongo-express  | [8081](http://localhost:8081/)  |


## Shut down and destroy

```
# Shut down the cluster
docker-compose down
```