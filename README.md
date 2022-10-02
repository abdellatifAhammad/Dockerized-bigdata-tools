---
title: 'docker - Big data tools project'
author: Abdellatif Ahammad
---

Docker Big data tools
===
![docker](https://img.shields.io/badge/docker-19.03.6-blue)
![dcoker-compose](https://img.shields.io/badge/docker--compose-1.17.1-orange)
![haoop](https://img.shields.io/badge/hadoop-%20-brightgreen)

:flag-ma:  the main principle of this repo is to have the complete tools of big data run on the way and ready to use. 
> :balloon: there are two ways there so you can choose anyone you want .

## 1- the Cloudera Manager and CDH quick start
> this offers a Hadoop cluster from 2014, with Cloudera express manager (free version), that gives a nice experience to launch and stop any tool from its UI.
 
 
#### :black_nib: the tools that exist in this cluster  


| Name             | Port  |
| ---------------- | ----- |
| HDFS             | 8002  |
| Cloudera Manager | 7180  |
| Hue              | 8888  |
| Hive             | 10002 |
| Oozie            | 11000 |
| Zookeeper        | 2181  |
| Solr             | 8983  |
| Sqoop Metastore  | 16000 |
| Impala           |   -   |
| Spark Master     | 7077  |

#### quickstart :100: 
>  use only the  hadoop cluster without the cloudera manager :first_place_medal: 
```bash=
    git clone https://github.com/abdellatifAhammad/Dockerized-bigdata-tools
    cd docker-bigdata/cloudera_express
    sudo docker-compose up
```
> you will see something like this at the beginning
> ![](https://i.imgur.com/GvH33De.png)




>  use  the cluster with the cloudera manager :golf: 
>  inside the cloudera_express folder use this 
```bash=
    sudo docker attach abdo_cdh
    /home/cloudera/cloudera-manager --express
```
###### it  takes some time to be launched

#### Examples services UI  : 
> Hue
 ![](https://i.imgur.com/xMGl0gh.jpg)
> Hive inside Hue (hive editor)
![](https://i.imgur.com/RLZ0nEb.jpg)
>Impala
![](https://i.imgur.com/eUr5mI3.jpg)
>cloudera_manager Interface
> you have to launch the service that you want manually from this dashboard
![](https://i.imgur.com/5v6WFZc.jpg)
>HBase
![](https://i.imgur.com/DeM3YZc.jpg)

## 2 - big data tools without  CDH (only Docker Images from dockerhub ) 

> this one is a Hadoop cluster that contains multiple data nodes (just 3 in this docker-compose file you can make more of them)

###### I want to say thanks to the creators of these images in the docker hub :call_me_hand: 
>  - [fjardim](https://hub.docker.com/u/fjardim)
>  - [streamset](https://hub.docker.com/r/streamsets/datacollector) 
>  - [fmantuano](https://hub.docker.com/r/fmantuano/apache-storm)



### quick start

```bash=
    git clone https://github.com/abdellatifAhammad/Dockerized-bigdata-tools
    cd docker-bigdata/big_data
    sudo dcoker-compose up -d
```
then you can check all these nice  tools (check ports from the docker-compose file)
    
    - Hive
    - hue
    - zookeper
    - mysql
    - kafka
    - hbase
    - mongo
    - sqoop metabase
    - streamsets
    - storm
    
    





