footer: © GoDataDriven, Fokko Driesprong(@godatadriven.com), @fokkodriesprong

# Event Collection
## on the Google Cloud

![fit](npo.png)

---

![fit](uni.jpg)

# Whoami

- Master Distributed Systems & Software Engineering
- Apache PPMC Member and Apache Airflow committer
- Contributor to Apache Flink, Apache Spark, Apache Druid and more

---

![fit](smalllogo.png)

# GoDataDriven

- IT Consultancy company
- Data Engineering and Science
- Open source minded

---

![fit](kloud.png)

---

![](fokko-npo.png)

---

![](npo-without-border.jpeg)

---

![](npo-border.jpeg)


---

# Events coming from:


![inline](platforms.png)

---

![fit](luizen.png)

# Volumes
- ~10k requests per second
- ~1m unique visitors per day
- ~120m records per day
- Highly dynamic

---

# Divolte

![fit](divolte.png)

- Crazy fast, open source, event collector

```javascript
divolte.signal('searchResultClick', {
    productId: 309125,
    searchPhrase: 'sneakers'
})
```
- Apache Avro (with schema evolution)
- HDFS, Kafka, GCS and GCPS sink
- ip2geo Lookup

---

![inline](mapping.png)

---

# Rolling updates

![inline](kubernetes-fix.png)

---

![fit](divolte.png)

# Try it yourself

- Examples and documentation: Divolte.io
- Docker: https://hub.docker.com/r/godatadriven/divolte/
- Proof of concept: https://blog.godatadriven.com/divolte-kafka-druid-superset

---

![](npo-border.jpeg)


---

![](dataflow.png)

# Dataflow

- Consume Avro
- Remove corrupted/duplicates
- Run aggregations
- Push to Bigquery

---

# Dataflow CI

- Run: PMD, FindBugs, Unit-test 
- Jenkins builds new jar and deploys on staging
- If ok, deploy on production

```
java -jar ./build/libs/raw-aggregations.jar  \
                --jobName=${job}  \
                --runner=DataflowRunner  \
                --project=${project}  \
                --region=europe-west1  \
                --streaming=true  \
                --workerMachineType=n1-standard-8  \
                --maxNumWorkers=8  \
                --subscription=${subscription}  \
                --update=true \
                --autoscalingAlgorithm=THROUGHPUT_BASED
```


---

![fit](autoscaling.png)

---

![fit](looker.png)

---

![fit](kitchen.png)

---

![](flits.png)

---

![](npo-border.jpeg)

---

![](airflow.png)

# Apache Airflow

- Developed by Airbnb in 2015
- Programatically workflow scheduling
- {ETL, Machine Learning, Predictive, General} pipeline
- Great Google Cloud integration
- Used by 150+ companies, including Airbnb, ING, LinkedIn, Paypal
- ~350 contributors

---

![](avro-to-parquet.png)

---

![](airflow-job.png)

---

![](npo-without-border.jpeg)

---

# Next steps

- Running Spark on Kubernetes
- Faster feedback using Dataflow
- Apache Airflow on Kubernetes

![](spark8s.jpg)

---

# Thank you for your attention

## Time for questions!