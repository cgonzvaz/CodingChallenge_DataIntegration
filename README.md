# Coding Challenge Data Integration

This repository contains development code related to the Adidas challenge about Data Integration.

The Challenge is divided in two parts:

Challenge #I: The Basics
The eCommerce company owning the app would like to:
1) Reliably capture the incoming message stream where there could be large
fluctuations in the number of messages being received at a given time (eg sales on
Cyber Monday)
2) Queue the data for further processing
3) Parse the data to tabular structures
4) Forward the data to tables in a data warehouse for analysis and reporting teams

Challenge #2
You will replace the batch based architecture to go real time in data capture. For that you need to:
• Implement an API capable of recieving JSON objects and send those objets to three different queues. One to parse data into
tabular data load it in a DB engine, another one to store the same data in csv format, and a third one to log messages in text files.
All of them should be able to respond to an eventual big message load.
• Incorrect values should be handled sepparately to go to an error file.

[more_info](Challenge_Desc.pdf)

## Getting Started

All the testing was executed on lapton on Windows 10. 

### Prerequisites

You will need to install the next software por testing porposal 
* [Pentaho Data Integration 8.2](https://sourceforge.net/projects/pentaho/files/latest/download?aliId=137249511) 
* [kafka_2.11-2.2.0](https://kafka.apache.org/downloads) 
* [zookeeper-3.4.14](https://zookeeper.apache.org/releases.html)
* [jdk1.8.0_211](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

All the test were executed on Microsoft Windows 10.

### Installing

If you need help for installing software tools please follown the next links
* [Pentaho Data Integration Installation](https://help.pentaho.com/Documentation/8.2)
* [Kafka](https://kafka.apache.org/documentation/)
* [Zookeeper](https://zookeeper.apache.org/documentation.html)

[Instalation Problems](InstalationProblems.md)

### Technical Review

Technical analysis and propsed solutions
* [ETL Technical design](Technical_Review.pdf)

## How it works - Testing 

* [Challenge#1](challenge_1.md)
* [Challenge#2](challenge_2.md)


## Authors

* **Christian Gonzalez**

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details




