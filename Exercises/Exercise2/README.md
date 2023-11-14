# Basic Ingestion (I) - HTTP to File

In this exercise we will get "batch data" from an open data source and store into the file system:

HTTP service --> NiFi --> File

This will be the data source (Valencia Open Data - ValenBisi Availability):

* https://valencia.opendatasoft.com/explore/dataset/valenbisi-disponibilitat-valenbisi-dsiponibilidad

In that dataset, **look for the CSV URL**.

Some tips:

* Use the following processors
  * InvokeHTTP
  * PutFile
* Connect the processors with the "response" output, and terminate the others
* **WARNING**: Check the “SCHEDULING” when invoking the HTTP URL and set to something reasonable (e.g. 30 secs), otherwise we will saturate the server

# Resources

* Apache NiFi (local): https://localhost:8443/nifi
* Apache NiFi Documentation: https://nifi.apache.org/docs.html
* Valencia Open Data: http://gobiernoabierto.valencia.es
