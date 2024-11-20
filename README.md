### 4.4.1-impala_quickstart_hms

docker pull apache/impala:4.4.1-impala_quickstart_hms
Idk merre tovább..

### lépések

login to docker

docker run -d --name kudu-impala -p 21000:21000 -p 21050:21050 -p 25000:25000 -p 25010:25010 -p 25020:25020 apache/kudu:impala-latest impala

download this(githhub repo included)
https://www.cloudera.com/downloads/connectors/impala/jdbc/2-6-15.html
useing JBDC: ImpalaJBDC42.jar

download this
https://dbeaver.io/download/

run

connect to database: cloudera impala

add JBDC driver, [IMG]

Kuka ez is


