# apim-data-populator
This JMeter script will populate sample data in WSO2 API Manager.

# Getting Started
1. Download and setup Apache JMeter from https://jmeter.apache.org/download_jmeter.cgi
    1. For linux users: download the zip file, goto bin directory, and run command `./jmeter`
2. Download or clone https://github.com/binodmx/apim-data-populator.git
3. Open `APIM Data Populator Plan <apim-version>.jmx` in JMeter
4. Goto APIM Data Populator Plan → User Defined Variables and change `adp_home` variable to path to apim-data-populator directory
5. Click on start button

Note:

APIM should be running in background with following configs
```
[apim.devportal]
enable_cross_tenant_subscriptions = true
enable_application_sharing = true
application_sharing_type = "default"
```

# Starting WireMock Server
1. Goto ../apim-data-populator/wiremock-server/
2. Locate wso2carbon.jks and wiremock-jre8-standalone-2.33.2.jar
3. Start the WireMock server by this command

```
java -jar wiremock-jre8-standalone-2.33.2.jar --port 8090 --https-port 8091 --https-keystore wso2carbon.jks  --keystore-password wso2carbon --key-manager-password wso2carbon
```

4. To test, call http://localhost:8090/hello or https://localhost:8091/hello 