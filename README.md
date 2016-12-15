# Table of contents
- [Test strategy](#test-strategy)
    + [Purpose](#purpose)
  * [Resources](#resources)
  * [Strategy](#strategy)
      - [Testing types](#testing-types)
    + [Risks](#risks)
    + [Project milestones](#project-milestones)
    + [Deliverables](#deliverables)
- [Test plan](#test-plan)
    + [Purpose](#purpose-1)
    + [Background](#background)
    + [Goals](#goals)
    + [Scope](#scope)
    + [Risks](#risks-1)
    + [Prioritization](#prioritization)
    + [Req for tests](#req-for-tests)
  * [Test Cases](#test-cases)
        * [Start server](#start-server)
        * [High load](#high-load)
        * [HTTP 1.1 Status 200](#http-11-status-200)
        * [HTTP 1.1 Status 404](#http-11-status-404)
        * [HTTP 1.1 Status 400](#http-11-status-400)
        * [HTTP 1.1 Status 403](#http-11-status-403)
        * [Access logs](#access-logs)
        * [Request image](#request-image)
        * [Shutdown server](#shutdown-server)
        * [HTTP 1.1 Status 405](#http-11-status-405)
        * [HTTP 1.1 HEAD](#http-11-head)
- [Test report](#test-report)
    + [Test results](#test-results)
      - [Automated tests](#automated-tests)
      - [Manual tests](#manual-tests)
      - [Test evaluation](#test-evaluation)
        * [--Automated--](#--automated--)
        * [--Manual--](#--manual--)
  * [Summary](#summary)
- [References](#references)

# Test strategy
### Purpose
This document if for our Product owner, SDC. SDC wants an easy to deploy java-webserver. The test strategy is to make sure the webserver can be deployed on many different devices. SDC wants to attract attention of IOT(Internet of things)-developers. The end-customers wants an easy access and absolute security.




Stakeholder:
* SDC: wants to know if the "My Web Server" fulfills their goals of an easy deploy java webserver that can be deployed on many different devices.


___


## Resources


**Roles and responsibilities**
* Test  lead
    * Has the responsibility of the test planning.
    * Makes sure the team has all the necessary resources to fulfill their responsibilities.
* Test engineers x2
    * Has to understand what needs to be tested.
    * Creates test cases from the test plan
* Test executor
    * Has the responsibility to make sure that all the test will be executed.
    * Reports defects on executed tests.




**Time budget**


Four people working half time, 20 hours/week, calculates to 160 hours for all four team members.




**Equipment**


* Operating systems: Windows, linux, mac
* Stress testing tool - jMeter
* Chrome plugin Postman




**Test computers requirements**


The test computer must have the latest operating system and the following programs installed:
* Java -v
* Terminal
* Text editor
___




## Strategy


#### Testing types


**1 _Compatibility_**


| | | 
|-|-|
|__Test Objective__|Because of the requirement "Deploy on many devices" we'll test the webserver on three different operating systems.|
|__Technique__|Deploy My Web webserver on three different operation systems|
|__Compleition criteria__|My Web webserver works the same on all the different operating systems|




**2 _Stress testing_**


| | | 
|-|-|
|__Test Objective__|Make sure that the webserver works on heavy load.|
|__Technique__|Use jMeter to test the webserver under heavy load.|
|__Compleition criteria__|The My Web webserver is still responsive in relative amount of time.|




**3 _Automated testing_**


| | | 
|-|-|
|__Test Objective__|Review and run the already existing Unit-tests for specific parts of the functionality of the system.|
|__Technique__|Examine and execute Unit test in My Web Server.|
|__Compleition criteria__|All the unit test pass.|




**4 _Manual testing_**


| | | 
|-|-|
|__Test Objective__|Testing the system with the human mind to find the bugs that the automated tests failed to cover.|
|__Technique__|The test executor will go through all the user cases.|
|__Compleition criteria__|The test executor will not find any abnormalities.|




**5 _Intergration testing_**


| | | 
|-|-|
|__Test Objective__|Making sure that the whole system works together. Testing to see that all the functions in the system adds up to one whole system. Make sure that the modules in the system are combined and tested as a group.|
|__Technique__|Use the system as the end-user will.|
|__Compleition criteria__|System does not produce any bugs or crash.|




**6 _Install /uninstall testing_**


| | | 
|-|-|
|__Test Objective__|Finding out what the end-user will need to do to install/uninstall and set up/remove the system.|
|__Technique__|Install/uninstall and set up/remove the system as the end user will.|
|__Compleition criteria__|System does not produce any bugs or crash. The system will be installed/uninstalled successfully.|








### Risks


**Security**


All connections should be encrypted and over a secure line.
No data should be leaked.
Skills and talent in the team is not enough.




**Availability**


The system should have an uptime of 99.9%.




### Project milestones


Effort hours is combined for all members in the team.


|Milestone task|Effort|Start Date|End Date|
|-|-|-|-|
|Plan test|20h|2016-11-28|2016-12-30|
|Design test|40h|2016-12-1|2016-12-06|
|Implement test|30h|2016-12-7|2016-12-10|
|Execute test|15h|2016-12-12|2016-12-13|
|Evaluate test|45h|2016-12-14|2016-12-20|
|Look over documentation|10h|2016-12-21|2016-12-22|




### Deliverables


__Test strategy__


The test strategy will define the technique that will be used to produce the tests.




__Test plan__


The test plan will define all the test cases and reference the requirement to each test case.




__Test cases__


The test cases will define the structure and steps needed to execute the test.




__Test report__


A final review of the tests will be presented. Did the tests show that the webserver worked as specified? 


___




# Test plan


### Purpose


The purpose of this test plan is to know if the system fulfills the requirements as stated in the requirements. (See reference list)




### Background


The My Web webserver allows the users to easily deploy a Java webserver on a wide range of devices. 




### Goals


SDC aims to redistribute this webserver on a wide range of Internet Of Things.
SDC wants an easy deploy java-web-server that can be deploys on many different devices.
IOT-developers want minimal configuration as well as easy integration and adaption of the web-server.
End-customer wants easy access and absolute security.




### Scope


Unit Testing will be used to check that the functionality still works. 
Manual Testing will be used to test the different scenarios in the use cases.




### Risks


* Not access or knowledge to all operating system specified in the requirements (See reference list).
* Test executor is unavailable and therefore cannot continue writing test reports.
* Human factor in the test executor can complicate the testing process.
* Not enough knowledge in programming language Java.




### Prioritization


|Test case id|Name|Priority level|
|-|-|-|
|0|Start server|High|
|8|Stop server|High|
|2|HTTP 1.1 Status 200|High|
|3|HTTP 1.1 Status 404|High|
|1|High load|Medium|
|4|HTTP 1.1 Status 400|Medium|
|5|HTTP 1.1 Status 403|Medium|
|6|Access logs|Medium|
|7|Request image|Medium|




### Req for tests


In the document "Web  Server, Requirements", all the requirements for the system is listed.
(See reference list)




## Test Cases


##### Start server


id: __0__
Requirement id: __3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: (hyper link to test computer req)




__Description__


The webserver should always start on the operating systems in requirement 3.




__Test steps__


Primary flow
1. Administrator starts Webserver
2. Webserver asked for port number and shared resource container
3. Administrator provides a port number and a shared resource container
4. Webserver stars on given port



Alternative  flow
2. a. Webserver does not asks for a port or a shared resource container.
    - Webserver does not start without right arguments.


2. b. Webserver only asks for a port
     - Webserver does not start without right arguments.


2. c Webserver only askes for a shared resource container
    - Webserver does not start without right arguments.


3. a. Administrator provides illegel port
    - Server craches


3. b. Administrator provides a port that is already in use
    - Server craches


3. c. Administrator does not provide any port at all
    - Server craches


3. d. Administrator provides a resource container that does not exist
    - Server present an error message:  “No access to folder XX”


3. e. Administrator does not provide a resource container
    - Server craches


4. a. Webserver does not start on given port
    - Webserver does not start 


__Expected results__


The webserver starts without any problems.


___




##### High load


id: __1__
Requirement id: __1__
Category: __Non functional test__
Test type: __Stess test__
Executed and reported by: __The Test executor__
Pre-conditions: Test case 0




__Description__


Server should work on heavy load. 100 connections 20 times.




__Test steps__


Primary flow
Input: 100*20, 2000*20
1.  The 'input amount' of connections is connecting to the server
2.  The webserver is still responsive




Alternative flow
connector = User that wants to connect
2.a The webserver is not responsive on the input amount
    - The 'connector' has to wait a long time for a response
    - The 'connector' gets an error message about the servers timeout




__Expected results__


The webserver is still responsive


___




##### HTTP 1.1 Status 200


id: __2__
Requirement id: __2, UC3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,




__Description__


The webserver are able to send a respond with HTML and a status code of 200.




__Test steps__


Primary flow
1. User sends a request to the start page of the server
2. User gets a status code 200 - OK




Alternative flow
2a. User does not get any HMTL or 200 status code
2b. User gets 200 but not any HMTL
2c. User gets HTML but not status code 200




__Expected results__


User gets HTML and a response code of 200 from the server
___




##### HTTP 1.1 Status 404


id: __3__
Requirement id: __2, UC3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,




__Description__


The webserver are able to send a response with status code of 404.




__Test steps__


Primary flow
1. User sends a request to a page that does not exist
2. User gets a response code 404 - NOT FOUND




Alternative flow
2a. User does not get any HTML and status code of 404.




__Expected results__


User should get a response code of 404


___




##### HTTP 1.1 Status 400


id: __4__
Requirement id: __2, UC3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,




__Description__


The webserver are able to send a response with status code of 400.




__Test steps__


Primary flow
1. User sends a POST-request with invalid body-data to the server
2. User gets HTML and response code 400 - BAD REQUEST




Alternative flow
2a. User does not get any HTML and status code of 400.




__Expected results__


User should get a response code of 400


___




##### HTTP 1.1 Status 403


id: __5__
Requirement id: __2, UC3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,




__Description__


The webserver are able to send a respond with HTML and specified status codes.




__Test steps__


Primary flow
1. User sends a request to a forbidden resource on the server
2. User gets HTML and response code 403 - FORBIDDEN




Alternative flow
2a. User does not get any HTML and status code of 403.




__Expected results__


User should get a response code of 403


___




##### Access logs


id: __6__
Requirement id: __5__
Category: __Non functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: 




__Description__


When a request with information is sent to the server, a note in the access logs is written about the sent request.




__Test steps__


Primary flow
1. A request is sent to the server
2. A note is written to the access log
3. The access log is viewable in a text-editor


Alternative flow
2a. Nothing is written in the access log
    - The system provides an error message and when a user opens the access log it's empty or not updated. 
2b. The access log is not created
    - The user cannot find the access log and the server present an error message
3a. The access log is created in the wrong format
    - The user cannot open the access log in a text editor


__Expected results__


All the request to the webserver are logged in the access log.
The written notes will be viewable for the user in a text editor.

___


##### Request image


id: __7__
Requirement id: __UC3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,


__Description__


Server should be able to return a image upon a request.


__Test steps__


Primary flow
1. A request for an image is made.
2. The webserver responses with an image.


Alternative flow
2.  a. The webserver does not respond with an image.


__Expected results__


The webserver responses with an image.


___



##### Shutdown server


id: __8__
Requirement id: __UC2__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,




__Description__


An system administrator should be able to stop the server.




__Test steps__


Primary flow
1. Administrator chooses to stop the server
2. The webserver stops and presents a message




Alternative flow
2. a. The webserver is still on








2. a. The webserver does not present a message




__Expected results__


The webserver stops and presents a message about that the webserver has been stopped.


___




##### HTTP 1.1 Status 405


id: __9__
Requirement id: __2, UC3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,




__Description__


The webserver are able to send a response with status code of 405.




__Test steps__


Primary flow
1. User sends a POST-request to the root
2. User gets HTML and response code 405 - POST NOT SUPPORTED




Alternative flow
2. a. User does not get any HTML and status code of 405.




__Expected results__


User should get a response code of 405.


___


##### HTTP 1.1 HEAD


id: __10__
Requirement id: __2, UC3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,




__Description__  


Check the HTTP 1.1 head method.




__Test steps__


Primary flow
1. Send HEAD request to the webservers root.
2. Webserver responds with 200 - OK




Alternative flow
2. a. Webserver responds with another status code.




__Expected results__


Server should respond with a code of 200.


___




# Test report
### Test results
#### Automated tests


|Test|Status|OS|Date|
|-|-|-|-|
|AcceptThreadTest|passed|MacOS, Windows*, Linux|2016-12-12|
|ClientSocketTest|passed|MacOS, Windows*, Linux|2016-12-12|
|ClientThreadTest|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTPReaderTest|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTPRequestParserTest|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTPRequestTest|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTPServerConsoleTest|passed|MacOS, Windows*, Linux|2016-12-12|
|HeaderTest|passed|MacOS, Windows*, Linux|2016-12-12|
|PortTest|passed|MacOS, Windows*, Linux|2016-12-12|
|ResponseFactoryTest|passed|MacOS, Windows*, Linux|2016-12-12|
|ServerFactoryTest|passed|MacOS, Windows*, Linux|2016-12-12|
|SharedFolderTest|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTPServerTest|passed|MacOS, Windows*, Linux|2016-12-12|
|SocketClientTest|failed on all OS|MacOS, Windows*, Linux|2016-12-12|
|StressTest|passed|MacOS, Windows*, Linux|2016-12-12|
|ContentTypeTest|passed|MacOS, Windows*, Linux|2016-12-12|
|ErrorResponses|passed|MacOS, Windows*, Linux|2016-12-12|
|HTMLFileResponseTest|passed|MacOS, Windows*, Linux|2016-12-12|
|ConsoleViewTest|psssed|MacOS, Windows*, Linux|2016-12-12|


*XP, Vista, 7, 8, 10, server 2008


#### Manual tests


|Test case|Tc id|Status|OS|Date|
|-|-|-|-|-|
|Start server|0|failed|MacOS, Windows*, Linux|2016-12-12|
|High load 100*20|1|passed|MacOS, Windows*, Linux|2016-12-12|
|High load 2000*20|1|failed|MacOS, Windows*, Linux|2016-12-12|
|HTTP 1.1 Status 200|2|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTP 1.1 Status 404|3|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTP 1.1 Status 400|4|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTP 1.1 Status 403|5|failed|MacOS, Windows*, Linux|2016-12-12|
|HTTP 1.1 Status 405|9|passed|MacOS, Windows*, Linux|2016-12-12|
|Access logs|6|failed|MacOS, Windows*, Linux|2016-12-12|
|Request image|7|passed|MacOS, Windows*, Linux|2016-12-12|
|Shutdown server|8|passed|MacOS, Windows*, Linux|2016-12-12|
|HTTP 1.1 HEAD|10|failed|MacOS, Windows*, Linux|2016-12-13|


*XP, Vista, 7, 8, 10, server 2008


#### Test evaluation
##### --Automated--
__SocketClientTest__
* Socket Client test failed beacuse it tried to connect to a server that is not online.
To test if it was 'My webserver' was causing the problem the test executer changed the URL of the socket client test to a server that was online and responding. 
This resulted in in a successful response but it was the wrong headers since the headers in the test were hard coded.
From that the test executer concluted that the problem is not located in the 'My web server'.

##### --Manual--
__Start server, id: 0__
* Webserver does not ask for a port or a resource container when administror starts the webserver.
* When the adiminstror provides a legal and not in use port and legal resource container as program-argument s the server starts as expected.
* When the adiminstror provides a resource container that does not exist the server does not present an error message.


__High load, id 1__


* Served 100 request 20 times, all went fine
* Served 2000 request for 20 times, 10134 timed out and failed


__HTTP 1.1, id 2, 3, 4, 9__


* Webserver does not fully support HTTP 1.1
* All request methods is not implemented
    * Request for HEAD should get 200
    * Request for an image-folder should return 403
    

__HTTP 1.1, id 5__
* When request to image-folder webserver throws an error that is not handled, should get status code of 403

__Access log, id 6__
* Access log is not written when a connection is made to the server

__Request image, id 7__
* Trying to request an image directly works as expected.

__Shutdown server, id 8__
* Stopping the server works as expected.

__HTTP 1.1 HEAD, id 10__
* When a request was made to the HEAD the server reponed with a statyus code of 405.
This problem is not likey to cause any problem of the release of the server.

## Summary
After a executing all the tests on My Webserver the test team has concluded that the server does not fulfill all the requirements that SDC has provided.

This choise has been made beacuse of serveral reasons.
The My Web Server has too has many flaws. The system does not fulfill the requirments from SDC or its own use-cases. The problems in My Web Server is pretty easily fixed but there is too many of them and they would require too much work and maintenance.

The webserver is not actively maintained and therefor if any problems occur the SDC will have to stand for the costs and work to fix it. There will not be any new features and the server will not get imporved unless the SDC choose to do that themselfs.

The webserver could be easier to start, it does not go after the specified use-case for example. 

Beacuse the webserver does not fully support HTTP 1.1 the webserver is not suited for any type of usage. There is a clearly requirement about HTTP 1.1 that is specified in the requirement specification that the server does not fulfill.

The SDC specifies that the server should be realsed under GPL 2.0. My Web Server is now released under MIT. If the SDC wants to coninue to work on My Web Server they need to change it to GPL 2.0. To do that they need to contact the original developers.


After some research the test team have found what they think might be a more sutiable solution, to SDCs needs. The web of things framework from the W3C or Hello Blinky from Microsoft is two of the recomended solutions.  

---
# References


[Web  Server, Requirements](https://docs.google.com/document/d/1fgQngHIZ4_aGIeB2S9YOBCghcBN9EEKBiaN-71MbGac/edit#heading=h.asfyqmcdgxbh)




TODO: change 'user' in test case
















