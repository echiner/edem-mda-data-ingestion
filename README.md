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

* [Apache NiFi](http://localhost:8080/nifi)
* [NiFi Registry](http://localhost:18080/nifi-registry)

## Exercises

* [**Exercise 1**: Building our first Data Flow](Exercises/Exercise1)
* [**Exercise 2**: Basic Ingestion (I)](Exercises/Exercise2)
* [**Exercise 3**: Basic Ingestion (II)](Exercises/Exercise3)
* [**Exercise 4**: GDELT Data Ingestion ](Exercises/Exercise4)
* [**Exercise 5**: Ingesting real-time data](Exercises/Exercise5)

## Understanding the components

Given that we will be reusing the same Docker Compose that we used in previous courses, we will have the same components (NameNode, DataNode, etc.), but in our case we will focus on the following:

* **Apache NiFi**: Ingestion tool used in the course
* **Apache NiFi Registry**: Code management and repository for Apache NiFi

Here is the list of components and ports:

| Component  | Ports |
| ------------- | ------------- |
| Apache NiFi  | 8080  |
| Apache NiFi Registry  | 18080  |

## Shut down and destroy

```
# Shut down the cluster
docker-compose down
```