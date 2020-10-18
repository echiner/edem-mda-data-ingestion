# Ingesting real-time data

In this exercise we will read data in real-time (e.g. Twitter), and store in HDFS:

Twitter --> NiFi --> HDFS

Mandatory:
* Read from a real-time data source
* Apply some internal processors (e.g. filtering, split, conversion, etc.)
* Store in HDFS

Optional:
* Make it available in Hive

Tip:
* [Apply for a Twitter developer account](https://developer.twitter.com/en/apply-for-access)

**IMPORTANT NOTE** (with regards to Twitter account creation): Beware that in some cases the creation of the Twitter Dev account can take a few days.

## Alternative real-time data sources

If you don't want to use Twitter, feel free to use any other real-time data source:

* https://www.quora.com/Where-can-I-find-public-or-free-real-time-or-streaming-data-sources
* https://blog.k2datascience.com/real-time-data-sources-for-data-engineering-projects-9bcff65c8468
* https://github.com/ColinEberhardt/awesome-public-streaming-datasets
* https://www.pubnub.com/developers/realtime-data-streams/

Or even, you can just read from a source of data which changes over time (e.g. stocks or weather), so you can schedule it every x seconds/minutes.
For example:

* https://openweathermap.org/api

## Alternative non real-time data source

If you don't want to use Twitter and you don't find any real-time data source, feel free to create any other *more or less complex" workflow.

# Deliverables

This is what you will have to deliver:

* Screenshot of the workflow
* Short explanation of what you did (data source, transformations, etc.)

# Resources

* Apache NiFi (local): http://localhost:8080/nifi
* Apache NiFi Documentation: https://nifi.apache.org/docs.html
* Apache NiFi Expresion Language Guide: https://nifi.apache.org/docs/nifi-docs/html/expression-language-guide.html 
