# Challenge #1

Main Points:

• Define the structure of the XML document.
• Create a batch process using ETL tool (PDI community edition) to parse the data and store it in tabular CSV files in a normalized
form.
• You need to source and destination data files and the PDI package.
• The ETL job must handle failure rolling back the changes and send a success/failure notification to an email address.
• A second ETL must move normalized data to some datawarehouse csv files using a schema optimized for reporting.

Bonus points:
• You are free to add more attributes to the JSON source to build a richer table structure.
• ETL could process correct records and derive incorrect ones to an error file

## Getting Started

Once you have installed your PDI tool, you have to unzip the [file](files.7z) in your install directory.
For exameple in my test we have our install directory on my desktop

cd 'C:\Users\cgonza\Desktop\data-integration'
unzip files.7z

This will create a directory named files in your install directory

cd files

In the files directory you will find the next directories:
For the Challenge#1 only need the following folders:

* csv - this folder saves the csv output of the transformation
* json - this folder contains the input json of the transformation
* xml - this folder contains the output xml of the transformation process
* error - this folder contains the error output of the transformation process

In the files directory you can find the transformation and jobs generated for testing. 

* test_3.ktr - this transformation process contains all the transformations for the Challenge#1
* test_3.ktr.kjb - this job call the transformation before, send email and control errors.

## Running the tests

Execute PDI from your directory installation

**C:\Users\cgonza\Desktop\data-integration>Spoon.bat**

Then you have to open the test_3.ktr.kjb and run.
This job will create 2 files:
* a csv file with all the transformation in the csv folder - data.csv
* a xml file with all the xml estructure data in the xml folder - 





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

