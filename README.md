# Test strategy
### Purpose
This document if for our Product owner, SDC. SDC wants an easy to deploy java-webserver. The test strategy is to make sure the webserver can be deployed on many different devices. SDC wants to attract attention of IOT(Internet of things)-developers. The end-customers wants an easy access and absolute security.

Stakeholder:
* SDC: wants to know if the "My Web Server" fulfills their goals of an easy deploy java webserver that can be deployed on many different devices.
___
## Resoruces
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
Four people working half time, 20 hours/week, calulates to 160 hours for all four team members.

**Equipment**
* Operating systems: Windows, linux, mac
* Stress testing tool
* (FLER program)

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
|__Test Objective__|Because of the requirement "Deploy on many devices" we'll test the server on three different operating systems.|
|__Technique__|Deploy My Web Server on three different operation systems|
|__Compleition criteria__|My Web Server works the same on all the different operating systems|

**2 _Stress testing_**
| | | 
|-|-|
|__Test Objective__|Make sure that the server works on heavy load.|
|__Technique__|Use (PROGRAM) to test the server under heavy load.|
|__Compleition criteria__|The My Web Server is still responsive in relative amount of time.|

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
|__Test Objective__|Making sure that the whole system works together. Testing to see that all the functions in the system adds up to one whole system. Make sure thaht the modules in the system are combined and tested as a group.|
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
|Milestone task|Effort|Start Date|End Date|
|-|-|-|-|
|Plan test|20h|2016-12-06|2016-12-22|
|Design test|40h|2016-12-06|2016-12-22|
|Implement test|30h|2016-12-06|2016-12-22|
|Execute test|25h|2016-12-06|2016-12-22|
|Evaluate test|45h|2016-12-06|2016-12-22|

### Deliverables
__Test strategy__
The test strategy will define the technique that will be used to produce the tests.

__Test plan__
The test plan will define all the test cases and reference the requirement to each test case.

__Test cases__
The test cases will define the structure and steps needed to execute the test.

__Test report__
A final review of the tests will be presented. visade testerna att servern fungerade som tänkt?

# Test plan
### Purpose
The purpose of this test plan is to know if the system fulfills the requirements as stated in the requirements. (See reference list)


### Background
The My Web Server allows the users to easily deploy a Java webserver on a wide range of devices. 


### Goals
SDC aims to redistribute this server on a wide range of Internet Of Things.
SDC wants an easy deploy java-web-server that can be deploys on many different devices.
IOT-developers want minimal configuration as well as easy integration and adaption of the web-server.
End-customer wants easy access and absolute security.


### Scope
Unit Testing will be used to check that the functionality still works. 
Manual Testing will be used to test the different scenarios in the use cases.


### Req for tests
In the document "Web  Server, Requirements", all the requirements for the system is listed.
(See reference list)

|Functionality|Interface|
|-|-|
|||
(SKRIV OM VARJE TEST)
which requirements
functionality
interface(console)




prioritatzion
how should we test
what teconligy
who does the things with the tests?(implements, runs, has vital info, uses the results)
the risks


lists if test that failed and succeedded 





# Test Cases
##### Start server
id: __0__
Requirement id: __3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: (hyper link to test computer req)

__Description__
The webserver should allways start on the operating systems in requirement 3.

__Test steps__
Primary flow
1. Start web server with legal arguments.

Alternative  flow
1 __a.__ Start webserver with ilegal argument.
    - The server does not start and throws an error.
1 __b__ Start webserver with port that is already taken
    - The server does not start and throws an error.
1 __c__ Start webserver whitout any arguments.
    - The server does not start and throws an error.

__Expected results__
The server starts without any problems.
___
##### High load
id: __1__
Requirement id: __1__
Category: __Non functional test__
Test type: __Stess test__
Executed and reported by: __The Test executor__
Pre-conditions: Test case 0

__Description__
Server should work on heavy load.

__Test steps__
Primary flow
Input: 900, 9000, 90000
1.  The 'input amount' of connections is connecting to the server
2.  The server is still responisve

Alternative flow
connector = User that wants to connect
2.a The server is not responive on the input amount
    - The 'connector' has to wait a long time for a response
    - The 'connector' gets an error message about the servers timeout

__Expected results__
The server is still responsive
___
##### HTTP 1.1 Status 200
id: __2__
Requirement id: __2__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,

__Description__
The server are able to send a respond with HTML and a status code of 200.

__Test steps__
Primary flow
1. User sends a request to the start page of the server
2. User gets a status code 200 - OK

Alternative flow
2a. User does not get any HMTL or 200 status code

__Expected results__
User gets HTML and a response code of 200 from the server

___
##### HTTP 1.1 Status 404
id: __3__
Requirement id: __2__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,

__Description__
The server are able to send a respond with status code of 404.

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
Requirement id: __2__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,

__Description__
The server are able to send a respond with status code of 400.

__Test steps__
Primary flow
1. User sends a POST-request with invalid information to the server
2. User gets HTML and response code 400 - BAD REQUEST

Alternative flow
2a. User does not get any HTML and status code of 400.

__Expected results__
User should get a response code of 400
___

##### HTTP 1.1 Status 403
id: __5__
Requirement id: __2__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: Test case 0,

__Description__
The server are able to send a respond with HTML and specified status codes.

__Test steps__
Primary flow
1. User sends a request to a forbidden resource on the server
2. User gets HTML and response code 403 - FORBIDDEN

Alternative flow
2a. User does not get any HTML and status code of 403.

__Expected results__
User should get a response code of 403
___

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
    - When a users opens the access log its empty or not updated.
2b. The access log is not created
    - The user cannot find the access log
3a. The access log is created in the wrong format
    - The user cannot open the access log in a text editor


__Expected results__
All the request to the server ar logged in the access log.
The witten notes will be viewable for the user in a text editor.
___

# References
[Web  Server, Requirements](https://docs.google.com/document/d/1fgQngHIZ4_aGIeB2S9YOBCghcBN9EEKBiaN-71MbGac/edit#heading=h.asfyqmcdgxbh)


id: __0, Start server__
Requirement id: __3__
Category: __Functional test__
Test type: __Manual test__
Executed and reported by: The Test executor
Pre-conditions: (hyper link to test computer req)

__Description__


__Test steps__
Primary flow

Alternative flow

__Expected results__


CHANGE: user in test case
