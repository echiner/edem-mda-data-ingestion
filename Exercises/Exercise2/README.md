# Basic Ingestion (I)

In this exercise we will get "batch data" from an open data source and store into the file system:

HTTP service --> NiFi --> File

This will be the data source (Valencia Open Data):

* https://www.valencia.es/dadesobertes/es/dataset/?id=textos-dels-carrers 

In that dataset, look for the CSV URL.

Some tips:

* Use the following processors
  * InvokeHTTP
  * PutFile
* Connect the processors with the "response" output, and terminate the others
* WARNING: Check the “SCHEDULING” when invoking the HTTP URL and set to something reasonable (e.g. 30 secs), otherwise we will saturate the server

# Resources

* Apache NiFi (local): http://localhost:8080/nifi
* Apache NiFi Documentation: https://nifi.apache.org/docs.html
* Valencia Open Data: http://gobiernoabierto.valencia.es
