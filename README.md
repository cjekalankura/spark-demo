spark-demo
note: this was forked from granthenke/spark-demo (https://github.com/granthenke/spark-demo)
==========

How To Build:
1. Execute ```docker-compose up -d```
1. Execute ```docker-compose exec builder /bin/bash```
1. Once inside the `builder`, execute ```gradle build```
1. Execute ```docker-compose exec spark /bin/bash```
1. Once inside the `spark`, execute ``` spark-submit \
--class com.cloudera.sa.SparkPi \
--master yarn-client \
--driver-memory 1g \
--executor-memory 1 \
--executor-cores 1 \
/libs/sparkify-1.0-SNAPSHOT-hadoop.jar local[2] 100 ```
