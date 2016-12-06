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










# References
[Web  Server, Requirements](https://docs.google.com/document/d/1fgQngHIZ4_aGIeB2S9YOBCghcBN9EEKBiaN-71MbGac/edit#heading=h.asfyqmcdgxbh)







