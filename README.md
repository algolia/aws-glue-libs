# aws-glue-libs
This repository contains libraries used in the [AWS Glue](https://aws.amazon.com/glue) service. These libraries extend [Apache Spark](https://spark.apache.org/) with additional data types and operations for ETL workflows. They are used in code generated by the AWS Glue service and can be used in scripts submitted with Glue jobs. 

## Content

- [awsglue](awsglue) -- This Python package includes the Python interfaces to the AWS Glue ETL library.

## Running gluepyspark shell, gluesparksubmit and pytest locally

The Glue ETL jars are now available via the maven build system in a s3 backed maven repository. We use the copy-dependencies target in
maven to get all the dependencies needed for glue locally.

Install apache maven from the following location:
http://apache.mirrors.tds.net/maven/maven-3/3.6.0/binaries/apache-maven-3.6.0-bin.tar.gz

Install the spark distribution from the following location:
https://archive.apache.org/dist/spark/spark-2.2.1/spark-2.2.1-bin-hadoop2.7.tgz

Export SPARK_HOME environment variable to extracted location of the
above spark archive.(ex: export SPARK_HOME=/home/$USER/spark-2.2.1-bin-hadoop2.7)

The gluepytest script assumes that the pytest module is installed and available in the PATH

Glue shell: ./bin/gluepyspark
Glue submit: ./bin/gluesparksubmit
pytest: ./bin/gluepytest

## Licensing

The libraries in this repository licensed under the [Amazon Software License](http://aws.amazon.com/asl/) (the "License"). They may not be used except in compliance with the License, a copy of which is included here in the LICENSE file.
