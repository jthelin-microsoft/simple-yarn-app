simple-yarn-app
===============

Simple YARN application to run n copies of a unix command - deliberately kept simple (with minimal error handling etc.)

Usage:
======

### Unmanaged mode

```
$ hadoop jar $HADOOP_YARN_HOME/share/hadoop/yarn/hadoop-yarn-applications-unmanaged-am-launcher-2.6.0.jar Client -classpath simple-yarn-app-1.1.1.jar -cmd "java com.hortonworks.simpleyarnapp.ApplicationMaster /bin/date 2"
```

### Managed mode

```
$ hadoop fs -copyFromLocal simple-yarn-app-1.1.1.jar /apps/simple/simple-yarn-app.jar
```

```
$ hadoop jar simple-yarn-app-1.1.1.jar com.hortonworks.simpleyarnapp.Client /bin/date 2 /apps/simple/simple-yarn-app.jar
```
  
    
