# Spark on Kubernetes Docker Image

In order to get a working image of Apache Spark 2.4.4 for K8s:
```   
    git clone https://github.com/apache/spark.git
    git checkout tags/v2.4.4
    build/mvn -Pkubernetes -DskipTests clean package
    ./bin/docker-image-tool.sh -r <repo> -t my-tag build
    ./bin/docker-image-tool.sh -r <repo> -t my-tag push
````

