# Welcome to the Nexpose App for Splunk
This Splunk App will give you an Insight of the Rapid7 Nexpose logs by using various Knowledge object.

# About
Author: Avotrix
Version: 1.0.0

# Release Notes
Version 1.0.0: Initial Release

# Diagnostics Generation
Please include a support diagnostic file when creating a support ticket. Use the following command to generate the file based on which Splunk app or add-on is
      installed. Send the resulting file to support.
      •	$SPLUNK_HOME/bin/splunk diag --collect=app:  nexpose_app_for_splunk
      
# Installation
•	Software requirements:
    I.	Splunk Enterprise system requirements: This App runs on Splunk Enterprise hence all of the Splunk Enterprise system requirements apply

# Deployment Guide
    I.In Single Environment:
        a.Download the add-on from Splunkbase.
        b.Then Navigate to Apps>Manage App
        c.Click Install app from file.
        d.Locate the downloaded file and click Upload.
    
    II.Distributed Environment:
        a.Install the App on the Search Head.
        
# Populating Dashboard
To Populate the Dashboard kindly specify the index and sourcetype in below macros:
     For Vulnerability Input: `nexpose-vulnerability-index-and-sourcetype`
     For Asset Input: `nexpose-asset-index-and-sourcetype`
     For Scan Input: `nexpose-scan-index-and-sourcetype` -- Kindly refer to section mentioned below(Second Method to onboard logs) to know how onboard the data of this                       input.
     
# Second Method to onboard the nexpose logs
In this method we will be export the nexpose data to an exteranl database and then by using "Splunk DB Connect" we are going to pull the logs.
  - In the Nexpose Side to export the data, the setting can be found under: "Settings>Data warehouse".
  - This method can be used either with your current version of Nexpose or you can also download the 
  	  Nexpose community edition(https://www.rapid7.com/info/nexpose-community/).
  - The steps required to install "Nexpose community edition/Rapid7 nexpose" are mentioned in "Nexpose Community Edition Installation" directory in the repo.
  - The document in the directory also contains the additonal steps you have to keep in mind when exporting the nexpose data to external postgress database.
  - After you have exported the Nexpose Data to external database then install "Splunk DB Connect" on the Heavy Forwarder and use the queries mentioned in the
     "Queries" directory in the repo to pull the logs.
  - You can also create your own queries in "Splunk DB Connect" to pull data as per your requirement.



