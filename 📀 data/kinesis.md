## Kinesis Data Streams
Used to allow the large scale ingestion of data into AWS and the consumption of that data by other compute resources known as consumers.

## Kinesis Data Firehose
Provides delivery services. It accepts data in and then delivers it to supported destinations in **near real-time**. It can also use LAMBDA to perform transformation of that data as it passes thru.

#### Supported Destinations
* HTTP endpoints (it means it can deliver to third party providers)
* Splunk
* Redshift
* ElasticSearch
* S3

## Kinesis Data Analytics
* A service which provides **real-time** processing of data which flows thru it using the SQL. Data inputs at one side, queries run againts that data and then data is ouput to destinations at the other.
* Ingests from Kinesis Data Streams or Kinesis Data Firehose and can optionally pull in static data from S3.
* After data is processed, it can be sent on in real-time to other destinations

#### Supported Destinations
* Firehose (and other destinations that Firehose supports: S3, Redshift, ElasticSearch, Splunk) - when used the process becomes near real-time rather than real-time
* AWS Lambda
* Kinesis Data Streams - data delivery is real-time
