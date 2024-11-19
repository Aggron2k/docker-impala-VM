
### 4.4.1-impala_quickstart_hms
docker pull apache/impala:4.4.1-impala_quickstart_hms
Idk merre tovább..

### lépések
login

docker run -d --name kudu-impala -p 21000:21000 -p 21050:21050 -p 25000:25000 -p 25010:25010 -p 25020:25020 apache/kudu:impala-latest impala