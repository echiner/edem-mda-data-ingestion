# Basic Ingestion (II)

In this exercise we will get "batch data" from an open data source and store into HDFS, performing some "data preparation":

HTTP service --> NiFi --> HDFS

# Details

In this exercise we will not only move data (from HTTP to HDFS), but also do some basic transformations:

* Split the file, using the **SplitText** processor
  * Split every 1000 rows
* Rename the file, using the **UpdateAttribute** processor
  * Example renaming: `EDEM-${filename}-${nextInt()}.txt`

For storing into HDFS, we will be using the **PutHDFS** processor. Tip:

* The config file required in the config is already created under `/tmp/shared`

# Resources

* Apache NiFi (local): http://localhost:8080/nifi
* Apache NiFi Documentation: https://nifi.apache.org/docs.html
* Apache NiFi Expresion Language Guide: https://nifi.apache.org/docs/nifi-docs/html/expression-language-guide.html 
* Data Source: http://gobiernoabierto.valencia.es/es/resource/?ds=textos-calles&id=975c7bd7-7eef-4201-b8a2-3bdc45b0906e
