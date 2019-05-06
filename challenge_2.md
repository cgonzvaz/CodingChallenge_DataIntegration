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

csv - this folder saves the csv output of the transformation

json - this folder contains the input json of the transformation

xml - this folder contains the output xml of the transformation process

error - this folder contains the error output of the transformation process


In the files directory you can find the transformation and jobs generated for testing.

test_8.ktr - this transformation process execute the Kafka consumer

test_9.ktr - this transformation process get records from streaming and save the data


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

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

