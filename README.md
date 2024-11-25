# Cloudera-VM


[Letöltési link](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa3A3ZGVBSXFjMk8xckNhOTBOc3VYZVB4aXFaQXxBQ3Jtc0trdzBxUUZIaFBMdGlaZmNPcXlNZWdmNjhGVUgwbC1BQ2RhWGpuWlBfaFlPcWhlenYzT1I2YmhEdFcwclV6UjQ3eXo3dXNaU1ZDd0ZYUDRzMXR1YkoyMGdrSzlQTVVzTklJS1RadkhWN1hDMUFuY1o0OA&q=https%3A%2F%2Fdownloads.cloudera.com%2Fdemo_vm%2Fvirtualbox%2Fcloudera-quickstart-vm-5.13.0-0-virtualbox.zip&v=jT1q5YQ2cpw)


```
sudo /home/cloudera/cloudera-manager --express --force
```

https://quickstart.cloudera:7180

Username:cloudera
Password:cloudera

# Cloudera manager

## Kötelezően futó szolgáltatások az Impala számára:
#### HDFS (Hadoop Distributed File System)

Az Impala az adatok olvasásához és írásához használja az HDFS-t.
Ellenőrizd, hogy az HDFS elérhető és működik.
#### Hive Metastore

Az Impala a Hive Metastore-t használja a táblák és a metaadatok kezelésére.
A hive-metastore és a hive-server2 szolgáltatásoknak futniuk kell.
#### Impala Daemonok

Az Impala saját komponensei, amelyeknek futniuk kell:
Impala StateStore: A csomópontok közötti koordinációért felelős.
Impala Catalog Server: A metaadatokat kezeli.
Impala Server (Daemon): Maga az SQL-lekérdezéseket végrehajtó szolgáltatás.

#### ZooKeeper
Az Impala és más Hadoop-komponensek koordinációjához szükséges (különösen nagyobb klaszterekben).


## Javasolt további szolgáltatások a Cloudera QuickStart környezetben:
#### YARN (Yet Another Resource Negotiator)

Segít a Hadoop erőforrásainak kezelésében, és biztosítja a számítási kapacitást.
### Hue

Egy böngésző-alapú interfész az adatok kezelésére és az Impala/Hive lekérdezések futtatására.


# Hue
https://quickstart.cloudera:8888

A default adatbázisba tároljuk el az embereket
```
CREATE TABLE default.peoples (
    id INT,
    name STRING,
    age INT,
    country STRING
)
STORED AS PARQUET;
```

```
INSERT INTO default.peoples VALUES
(1, 'Alice', 30, 'USA'),
(2, 'Bob', 25, 'UK'),
(3, 'Charlie', 35, 'Canada');
```

```
SELECT * FROM default.sample_data;
```

