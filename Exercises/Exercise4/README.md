# GDELT Data Ingesiton

In this exercise we will load data from GDELT. The [**GDELT Project**](https://www.gdeltproject.org/) is a realtime network diagram and database of global human society for open research.

The GDELT Project monitors the world's broadcast, print, and web news from nearly every corner of every country in over 100 languages and identifies the people, locations, organizations, themes, sources, emotions, counts, quotes, images and events driving our global society every second of every day, creating a free open platform for computing on the entire world.

# Details

On this exercise you are on your own, but here are some recommendations:

1. Understand the data and how it is provided (format, frequency, etc.):
   * https://blog.gdeltproject.org/gdelt-2-0-our-global-world-in-realtime/
2. Plan how you will build your workflow
3. Start small: Develop first an end-to-end happy path
4. Complete the workflow and enhance it

Some other considerations:

* Store or send the files wherever you want (e.g. File, HDFS, Kafka...)
* Make sure you set the scheduling in order to get the updated data periodically
* High level steps are:
  1. Download the master file
  2. For every line (data type)
     * Download the zip file
     * Unzip the file
     * If you want to convert to individual records: Extract records and send (e.g. Kafka or Database)
     * If you want to store the file: Rename and store in folder

# Resources

* Apache NiFi (local): http://localhost:8080/nifi
* Apache NiFi Documentation: https://nifi.apache.org/docs.html
* Apache NiFi Expresion Language Guide: https://nifi.apache.org/docs/nifi-docs/html/expression-language-guide.html 
* Data Source: https://www.gdeltproject.org/
