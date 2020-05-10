# Spark Event Log Analysis

* Analyse spark event log JSON & extract metrics for SQL queries.
* Reads spark JSON as input and analyse metrics for queries. 

### Input

* Spark event log JSON file for application.
* Output directory path.

### Output

* CSV file containing job level & query level metrics.

#### Spark event log can be found in following ways:
* From hdfs path provided in spark-default.conf with property `spark.eventLog.dir`. Log JSON file will be present with job application ID as name.
* It can also be downloaded using spark history server host & port provided in spark-default.conf with properties `spark.yarn.historyServer.address` and the application id of the job. Below if the format to the url.
    * https://{host}:{port}/api/v1/applications/{application id}/logs/
