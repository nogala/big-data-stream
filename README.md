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

La salida se puede ver 

        IMAGE                                             COMMAND                  CREATED             STATUS                             PORTS                                        NAMES

        confluentinc/ksql-examples:5.3.1                  "bash -c 'echo Waiti…"   6 minutes ago       Up 6 minutes                                                                    ksql-datagen

        confluentinc/cp-enterprise-control-center:5.3.1   "/etc/confluent/dock…"   6 minutes ago       Up 23 seconds                      0.0.0.0:9021->9021/tcp                       control-center

        confluentinc/cp-ksql-cli:5.3.1                    "/bin/sh"                6 minutes ago       Up 6 minutes                                                                    ksql-cli

        confluentinc/cp-ksql-server:5.3.1                 "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       0.0.0.0:8088->8088/tcp                       ksql-server

        cnfldemos/kafka-connect-datagen:0.1.3-5.3.1       "/etc/confluent/dock…"   6 minutes ago       Up 23 seconds (health: starting)   0.0.0.0:8083->8083/tcp, 9092/tcp             connect

        confluentinc/cp-kafka-rest:5.3.1                  "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       0.0.0.0:8082->8082/tcp                       rest-proxy

        confluentinc/cp-schema-registry:5.3.1             "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       0.0.0.0:8081->8081/tcp                       schema-registry

        confluentinc/cp-enterprise-kafka:5.3.1            "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       0.0.0.0:9092->9092/tcp                       broker

        confluentinc/cp-zookeeper:5.3.1                   "/etc/confluent/dock…"   6 minutes ago       Up 6 minutes                       2888/tcp, 0.0.0.0:2181->2181/tcp, 3888/tcp   zookeeper


Wait 1 - 5 minutes and enter to the Control Center web interface at http://localhost:9021/ 

