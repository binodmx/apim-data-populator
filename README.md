# apim-data-populator
This JMeter script will populate sample data in WSO2 API Manager.

# Getting Started
1. Download and setup Apache JMeter from https://jmeter.apache.org/download_jmeter.cgi
2. For linux users: download the zip file, goto bin directory, and run ./jmeter
3. Download or clone https://github.com/binodmx/apim-data-populator.git
4. Open APIM Data Populator Plan.jmx in JMeter
5. Goto APIM Data Populator Plan → User Defined Variables and change variable values according to the APIM version
6. Disable not supported HTTP Requests for the APIM version
7. Click on start button (APIM should be running in background)
