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
    * Making sure the team has all the necessary resources to fulfill their responsibilities.
* Test engineers
    * Has to understand what needs to be tested.
    * Creates test cases from the test plan
* Test executor
    * Has the responsibility to make sure that all the test will be executed.
    * Report defects on executed tests.


**Time budget**
Four people working half time, 20 hours/week, calulates to 160 hours for all four team members.

**Equipment**
* Operating systems: Windows, linux, mac
* Stress testing tool
* (FLER program)

**Test computers**
The test computer must have the latest operating system and the following programs installed:
* Java -v
* Terminal
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
|__Test Objective__|Making sure that the whole system works together. Testing to see that all the functions in the system adds up to one whole system.|
|__Technique__|Use the system as the end user will.|
|__Compleition criteria__|System does not produce any bugs or crash.|

### Risks
**Security**
All connections should be encrypted and over a secure line.
No data should be leaked.

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



