
# learn-spark

Perform the following docker pull
```
sudo docker pull bicepjai/learn-spark:latest
```

## DockerFile Info

OS details
```
Linux 8f6fd63bbfc8 4.10.0-37-generic #41~16.04.1-Ubuntu SMP Fri Oct 6 22:42:59 UTC 2017 x86_64 GNU/Linux
```

combination of some docker files to set up learning platform for spark

The docker files used are
1. https://hub.docker.com/r/p7hb/docker-spark/~/dockerfile/
2. https://hub.docker.com/r/continuumio/anaconda3/~/dockerfile/
3. https://github.com/LearningJournal/Spark-Tutorials

The ports in the container opened up are

```
# SparkContext web UI on 4040 -- only available for the duration of the application.
# Spark master’s web UI on 8080.
# Spark worker web UI on 8081.
# Anaconda 8082
```
Please add `-p` options to open up ports as required.

Command to start the container `learn-spark`
```
sudo docker run -p 8082:8082 learn-spark
```

Command to open up new shells
```
sudo docker exec -it <running-container-id> bash
```

the password for the jupyter notebook is `123456`
