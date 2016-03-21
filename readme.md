## API Simulator

 


### Instruction on running the simulator

- Change the request and response in data.json file in mapping folder accordingly
- run jar file with the following command

```java -jar wiremock-1.56-standalone.jar --verbose```


### Sample Request and Response

- Request

    curl -i -X GET "http://127.0.0.1:8080/app/total-sales?from=12-01-2015&to=12-07-2015"

- Response 

HTTP/1.1 200 OK
Server: Apache-Coyote/1.1
X-Powered-By: Servlet 2.4; JBoss-4.2.2.GA (build: SVNTag=JBoss_4_2_2_GA date=200710221139)/Tomcat-5.5
Content-Type: applicaiton/json;charset=UTF-8
Content-Length: 454
Date: Tue, 21 Jul 2015 08:36:50 GMT

{
  "from": "2015-08-01",
  "to": "2015-08-29",
  "currency": "LKR",
  "dailySummary": [
    {
      "date": "2015-08-24",
      "currency": "LKR",
      "totalSales": "1650.50",
      "totalOrderCount": 2
    },
    {
      "date": "2015-08-26",
      "currency": "LKR",
      "totalSales": "550.00",
      "totalOrderCount": 1
    }
  ],
  "links": [
    {
      "rel": "http://api.apptizer.io:9098/reporting/totalsales/summary/business/APP_000001?from=2015-08-01&to=2015-08-29",
      "href": "self",
      "method": "GET"
    }
  ]
}



