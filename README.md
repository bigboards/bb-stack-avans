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

We have packaged the most common technologies as a [BigBoards stack](http://hive.bigboards.io/#/library/stack/google-oauth2-103728492012393057640/bb-stack-avans). With the click of a button you can install everything on your BigBoards device. Just head over to the [BigBoards Hive](http://hive.bigboards.io).

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

## Practical
You can login to the notebooks environment with the default BigBoards username (`bb`) and password (`Swh^bdl`)

### Made with ♡ for data!

You are free to use the content, presentations and resources from this stack. Do keep in mind that we have put an aweful lot of work in creating these artefacts: please mention us to spread the karma! 

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons-Licentie" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a> Avans stack by <a xmlns:cc="http://creativecommons.org/ns#" href="http://bigboards.io" property="cc:attributionName" rel="cc:attributionURL">BigBoards CVBA</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International Licence</a>.

Based on work from <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/bigboards/bb-stack-training" rel="dct:source">https://github.com/bigboards/bb-stack-training</a>
