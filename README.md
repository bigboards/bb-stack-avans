# Big Data Basics

*by [BigBoards](http://bigboards.io)*

This stack accompanies the Big Data course at [Avans Hogeschool](http://www.avans.nl/)
The Big Data course contains a practical project on how to build a complete **data processing pipeline**. The workshop is **hands-on** using a [BigBoards Cube](http://bigboards.io/orderprototype). You will be touching **several common Big Data technologies**.

The accompanying [repository](https://github.com/bigboards/bb-stack-avans), contains all the technologies, resources and solutions to complete the workshop.

During this workshop, you can

- **ingest** data from a rather large **relational database**
- **store** the raw data on **distributed file system** as your primary data;
- **restructure** the data for **easier analysis**;
- and finally apply **machine learning** to build e.g. a **recommendation engine**.

## Big Data technologies

We have packaged the most common technologies as the [Avans introduction to Big Data stack](http://hive.bigboards.io/#/library/stack/google-oauth2-104831076958946284701/bb-stack-avans). 
With the click of a button you can install everything on your BigBoards device. Just head over to the [BigBoards Hive](http://hive.bigboards.io) and create an account. 

The technologies which you can use to build your end-to-end data pipeline, are:

- [Apache Hadoop](https://hadoop.apache.org/) for distributed storage, processing and resource management, 
- [Apache Sqoop](http://sqoop.apache.org/) for ingestion of relational data, 
- [Apache Pig](https://pig.apache.org/) to write data transformations, 
- [Apache Hive](https://hive.apache.org/) to query data on the distributed filesystem, 
- [Apache Spark](http://spark.apache.org/) for lightning fast data processing, 
- [Apache Spark SQL](http://spark.apache.org/sql/) for uniform data access, 
- [Apache Spark MLlib](http://spark.apache.org/mllib/) for machine learning. 

For now, we still host the data external to the big data clusters.

## User access

To access the device and technologies, we have linke the installed UIs on the dashboards if the stack is installed:

- [Yarn]() allow the user to get status on running Hadoop applications.
- [HDFS]() allow the user to get status on HDFS and read-onlly access to the directory tree.
- [MR History]() allow the user to get status on finished Hadoop applications.  
- [Notebooks](https://jupyterhub.readthedocs.io/) notebooks to interactively write and run programs on your device. Available kernels:
    - [PySpark]() to interactively run Spark pipelines
    - [Terminal]() for command-line access. Simply run `hadoop-shell` for full access to the Hadoop environment, incl. Pig, Scoop and Hive
- [Hue-filesystem]() for web access to the HDFS file system (TBD)

## hadoop-shell via notebooks

1. Install the [Avans introduction to Big Data app](http://hive.bigboards.io/#/library/stack/google-oauth2-104831076958946284701/bb-stack-avans) on your device
1. Link to the Jupyter notebooks via the `Available Views` link and log in to the notebooks environment 
1. Login with the default BigBoards username (`bb`) and password (`Swh^bdl`). Take care on entering the password, because of 
the circumflex. If it doesn't work type it in a text editor and paste it into the password field.
1. From the `Files` tab, launch a new terminal with the `New` > `Terminal` drop-down menu at the right-hand side of the screen. This brings you to a terminal shell inside the hadoop cluster. 
1. Run `hadoop-shell` to initialize a bash shell with all path to command lines initialized.

As an example, run `pig` to get inside a Grunt shell and try the command `fs -ls /tmp` to list the HDFS temporary folder

## Hive query

1. Get into an `hadoop-shell` as explained in the previous paragraph
1. Run `beeline` to get into Hive's interactive query environment
1. Run `!connect jdbc:hive2://<device-name>-n2:10000` 
1. username `hive`
1. password `hive`
1. `CREATE TABLE pokes (foo INT, bar STRING);`
1. `LOAD DATA LOCAL INPATH '/opt/hive/examples/files/kv1.txt' OVERWRITE INTO TABLE pokes;`
1. `SELECT count(*) FROM pokes;`
1. Run some other experiments on pokes, e.g. `SELECT MIN(foo), MAX(foo) FROM pokes;`
1. `DROP TABLE pokes;` to clean up

### Made with ♡ for data!

You are free to use the content, presentations and resources from this stack. Do keep in mind that we have put an aweful lot of work in creating these artefacts: please mention us to spread the karma! 

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons-Licentie" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a> Avans stack by <a xmlns:cc="http://creativecommons.org/ns#" href="http://bigboards.io" property="cc:attributionName" rel="cc:attributionURL">BigBoards CVBA</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International Licence</a>.

Based on work from <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/bigboards/bb-stack-training" rel="dct:source">https://github.com/bigboards/bb-stack-training</a>
