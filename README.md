Install steps

	$ docker-compose up -d --build

Creating network "docker_default" with the default driver
Creating zookeeper ... done
Creating broker    ... done
Creating schema-registry ... done
Creating connect         ... done
Creating rest-proxy      ... done
Creating ksql-server     ... done
Creating control-center  ... done
Creating ksql-cli        ... done
Creating ksql-datagen    ... done

	$ docker ps 

CONTAINER ID        IMAGE                                             COMMAND                  CREATED             STATUS                             PORTS                                        NAMES
a1b988a43aa3        confluentinc/ksql-examples:5.3.1                  "bash -c 'echo Waiti…"   6 minutes ago       Up 6 minutes                                                                    ksql-datagen
e9810da22aa5        confluentinc/cp-enterprise-control-center:5.3.1   "/etc/confluent/dock…"   6 minutes ago       Up 23 seconds                      0.0.0.0:9021->9021/tcp                       control-center
2df2fea80366        confluentinc/cp-ksql-cli:5.3.1                    "/bin/sh"                6 minutes ago       Up 6 minutes                                                                    ksql-cli
51f7ff24c5f8        confluentinc/cp-ksql-server:5.3.1                 "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       0.0.0.0:8088->8088/tcp                       ksql-server
9ad841d0f64a        cnfldemos/kafka-connect-datagen:0.1.3-5.3.1       "/etc/confluent/dock…"   6 minutes ago       Up 23 seconds (health: starting)   0.0.0.0:8083->8083/tcp, 9092/tcp             connect
73bdd22bf1d3        confluentinc/cp-kafka-rest:5.3.1                  "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       0.0.0.0:8082->8082/tcp                       rest-proxy
738365664f01        confluentinc/cp-schema-registry:5.3.1             "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       0.0.0.0:8081->8081/tcp                       schema-registry
0a556194d356        confluentinc/cp-enterprise-kafka:5.3.1            "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       0.0.0.0:9092->9092/tcp                       broker
233ee08ba9e9        confluentinc/cp-zookeeper:5.3.1                   "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       2888/tcp, 0.0.0.0:2181->2181/tcp, 3888/tcp   zookeeper

Navigate to the Control Center web interface at http://localhost:9021/


