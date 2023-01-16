# Student Scores Project | Big Data Analytics w/ Hadoop and Apache Spark
 
 <img src = "https://hadoopinrealworld.com/wp-content/uploads/2017/09/Spark-vs-Hadoop-Comparison-Chart.png" width = "500">
 
## Table of contents
* [Background](#background)
* [Dataset](#dataset)
* [Goals](#goals)
* [Technologies](#technologies)
* [License](#license)
* [Author](#author) 

## Background 

This project shows the combined capabilities of Hadoop and Apache Spark for a project showing some statistics on a student score data set. The practice of combining the strong sides of these two projects (i.e., Hadoop HDFS + Apache Spark) is regarderd highly by the data teams in these days.

**What is Hadoop?**

The Apache Hadoop Project is an open source project and consists of four main modules:

*  HDFS – Hadoop Distributed File System.
*  MapReduce. The processing component of the Hadoop ecosystem. It scales horizontally and is slow as it uses data storage. In the last decade, professionals use Apache Spark or Flink instead of MapReduce.
*  YARN. Yet Another Resource Negotiator. It is used for computing resources and job scheduling.
*  Hadoop Common. Also called as Hadoop core providing support for all other Hadoop components.

Among these modules, this project focuses on Hadoop HDFS. It is the file system managing the storage of large data sets. It can handle both structured and unstructured data. Hadoop stores the data to disks using HDFS.

**What is Apache Spark?**

Apache Spark is an open source project. It uses RAM for caching and processing data ans is designed for fast performance. Resilient Distributed Dataset (RDD) is the data structure of Spark.  It consists of five main components:

*  Apache Spark Core. Spark Core is the basis and includes functions of *scheduling, task dispatching, input and output operations, etc.* 
*  Spark Streaming. It is used for processing of live data streams with data sources of Kafka, Kinesis, Flume, etc.
*  Spark SQL uses this component to gather information about the structured data and how the data is processed.
*  Machine Learning Library (MLlib) includes machine learning algorithms.
*  GraphX is for facilitating graph analytics tasks.

In this notebook, we use Apache Spark Core functions as it uses memory to speed up the computations.  

## Dataset

Dataset consists of student scores of different subjects in CSV file format. There are 40 rows of data and one header. It is relatively small for the sake of practicing functions. In big data world, data size can go up to petabytes. 4 columns are given below:

Student | Subject |	Class Score |	Test Score

## Goals

This notebook will walk you through the (1) data loading into HDFS format and (2) data processing with Spark. Here's the outline:

* Import functions
* Data load 
    * Parquet File + Gzip codec  
    We prefer Parquet in HDFS as it reads col by col, provides schema, is compressible and splittable. It is ideal for analytics  
    We prefer gzip codec as it provides good compression but is not splittable and provides moderate performance. It is good for analytical purposes.  
    * Schema optimization
* Data processing
    * Computing total score
    * Printing total score for physics
    * Computing avg total score
    * Finding student with highest score

## Technologies

Project is created with community version of [DataBricks](https://community.cloud.databricks.com). It is a free edition and requires signing up to the website. Selected cluster for this project is 11.3 LTS. It includes  

* Apache Spark 3.3.0
* Scala 2.12

Driver type includes 15.3 GB Memory, 2 Cores and 1 DBU.

## License

Distributed under the MIT License. See LICENSE.txt for more information.

## Author

[levist7](https://github.com/levist7)

---

