# Basic Ingestion (II) - HTTP to File, with data manipulation

In this exercise we will get "batch data" from an open data source and store into file, performing some simple "data preparation":

HTTP service --> NiFi --> File

# Details

In this exercise we will not only move data (from HTTP to File), but also do some basic transformations:

* Split the file, using the **SplitText** processor
  * Split every 1000 rows
* Rename the file, using the **UpdateAttribute** processor
  * Example renaming: `EDEM-${filename}-${nextInt()}.txt`

# Resources

* Apache NiFi (local): https://localhost:8443/nifi
* Apache NiFi Documentation: https://nifi.apache.org/docs.html
* Apache NiFi Expresion Language Guide: https://nifi.apache.org/docs/nifi-docs/html/expression-language-guide.html 
* Data Source: https://www.valencia.es/dadesobertes/es/dataset/?id=textos-dels-carrers 
