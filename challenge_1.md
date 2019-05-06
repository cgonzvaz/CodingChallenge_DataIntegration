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

**Then you have to open the test_3.ktr.kjb and execute run**

This job will create 2 files:
* a csv file with all the transformation in the csv folder - data.csv
* a xml file with all the xml estructure data in the xml folder - json_structure.xml

All the process errors will be save on errors folder

All the source files are configured with the path ${Internal.Transformation.Filename.Directory}.
This path refers where the ktr files are. In this case the ktr file are in our {instalation_directory}/files

If you need more detail about the jobs and transformation uses, please refer [technical_overview](technical_overview.pdf)
