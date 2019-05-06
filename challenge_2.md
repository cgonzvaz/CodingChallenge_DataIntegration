# Challenge #2 Bonus Points

Main Points:

You will replace the batch based architecture to go real time in data capture. For that you need to:

• Implement an API capable of recieving JSON objects and send those objets to three different queues. One to parse data into
tabular data load it in a DB engine, another one to store the same data in csv format, and a third one to log messages in text files.
All of them should be able to respond to an eventual big message load.

• Incorrect values should be handled sepparately to go to an error file.


## Getting Started

If you have executed Challenge#1 you don´t have to do anything at this point. You have all the folder directory created.
If you don´t follow the next instructions:

Once you have installed your PDI tool, you have to unzip the file in your install directory. For example in my test we have our install directory on my desktop

cd 'C:\Users\cgonza\Desktop\data-integration' unzip files.7z

This will create a directory named files in your install directory

cd files

In the files directory you will find the next directories: For the Challenge#1 only need the following folders:

**csv** - this folder saves the csv output of the transformation

**json** - this folder contains the input json of the transformation

**xml** - this folder contains the output xml of the transformation process

**error** - this folder contains the error output of the transformation process


In the files directory you can find the transformation and jobs generated for testing.


**test_8.ktr** - this transformation process execute the Kafka consumer

**test_9.ktr** - this transformation process get records from streaming and save the data


### Prerequisites

In this Challenge is necessary to create an API for ingest data near real-time. For this purpose we will use Kafka. 
We have installed kafka and Zookeeper on Windows for testing this part.

You need to install **java** jdk for executing Zookeeper and Kafka and set the %JAVA_HOME% and include the %JAVA_HOME%/bin into the %PATH%

then you have to execute **Zookeeper** 
On Windows it is necesarry to change in {ZOOKEEPER_HOME}/conf/zoo_sample.cfg 

dataDir=/tmp/zookeeper 

to you directory

dataDir={ZOOKEEPER_HOME}/data

Then you can execute Zookeeper:

**%ZOOKEEPER_HOME%/bin/zkServer.cmd**

**binding to port 0.0.0.0/0.0.0.0:2181**
 
Wi will open por 2181 on localhost
 
 
Then we have to execute **Kafka** por creating a producer that can generate the streaming info. 
 
You have to define the logs folder on your configuration

In %KAFKA_HOME/config/server.properties we have to change the parameter log.dirs to your logs folder.
For example:
 
**logs.dir={KAFKA_HOMEM}/logs**
 
Now, you can execute kafka:
 
**%KAFKA_HOME%\bin\windows\zookeeper-server-start.bat zookeper.properties**
 
**Kafka starts on localhost, port 9092**
 
Now we have to create a topic
 
kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic **test**
 
and creating a producer to ingest the streaming json:
 
**kafka-console-producer.bat --broker-list localhost:9092 --topic test < {pentaho_directory_instalation}\files\json\json_real_time.json**


## Running the tests

Once we have the producers working, we have to executing the consumer in our PDI tool.
So, open your pdi tool, and open and execute the **test8.ktr** transformation.
You have to execute the transformation while the producers are working. 

The test8.ktr call the transformation test9.ktr for receiving data and transforming it. 

If you need more detail from the process please check [technical_overview](technical_overview)

**--> at this time the queue division is pending**


