## What is selenium:

Selenium WebDriver is an automation tool/API used to automate web browsers programmatically.
                                      **(OR)**
Selenium WebDriver allows your Java/Python/other automation code to control a real browser like Chrome, Firefox, or Edge.

- This is a JAVA interface
- And this is an API

```
Webdriver(interface) ---> RemoteWebDriver (implements I) ---> Extends to ChromeDriver,EdgeDriver etc....
```
## Environment Setup:
**1. Download JAR files and attaching them to JAVA Project** **(Not Recommended)**
- Download all selenium jar files from official website.
- Extract and place them in C drive or somewhere else.
- Create a JAVA project and attach JAR files to that project by following below steps (Called Configure Webdriver)
  - right click on project
  - properties
  - Java Build Path
  - libraries
  - Class Path and all the JAR's
    
**2. Mavan Project**
- Create a Maven project check create a Simple project
<img width="360" height="311" alt="image" src="https://github.com/user-attachments/assets/ed4ceebb-8801-4fc6-a8a9-fdd3aa0f2c87" />

- GroupID - Project Name
- Artifact ID - Same as Project Name
- Configure WebDriver:
  - get dependency from Maven dependency offical website
  - and add then to POM.xml
  - Update Maven Project









