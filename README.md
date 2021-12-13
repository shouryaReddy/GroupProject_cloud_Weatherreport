## GroupProject_cloud_Weatherreport

# Team Members
+ Ritesh Reddy Manchi Reddy
+ Manjusha Dondeti
+ Shourya Reddy Katkam

# Weather Report 
This is about implementing classification algorithms on weather dataset using Spark and Python.

### The files used are as follows:
1. weather_prediction.py: This is a python code file along with Spark to implement linear regression using ordinary least squares estimate.

2. weatherHistory.csv: This is the input file which consists of the information about climatic conditions on an hourly basis of a particular year.

3. weather_report.txt: This is the output file generated.

## Steps to run weather_prediction.py code on DSBA-Hadoop cluster
1. Connect to Cisco AnyConnect VPN with hostname as dsba-hadoop.uncc.edu and login with ninernet credentials.
 
2. Open PuTTY and enter dsba-hadoop.uncc.edu as hostname and login with ninernet credentials.
 
3. Create a directory using the following command
```
$ hadoop fs -mkdir /user/username/data
```
4. Now open WinSCP and give the hostname as dsba-hadoop.uncc.edu and login with ninernet credentials. Get the file weatherHistory.csv from the local system to dsba-hadoop user specific folder.
 
5. Use the following command to put the file in the required input path.
```
$ hadoop fs -put weatherHistory.csv /user/username/data
```
 
6. Get the weather_prediction.py file to the working directory throught WinSCP.

7. Run the following command to execute the code on input files respectively. The output file with results will be generated.
```
$ spark-submit weather_prediction.py
```
