# OrangeHRM

## Overview
<b<OrangeHRM</b> Automation Testing is a project dedicated to automating the testing of the OrangeHRM (Human Resource Management System) using Selenium WebDriver and Java. The primary goal is to ensure the stability and reliability of the OrangeHRM web application by automating various test scenarios such as employee management, attendance tracking, recruitment, leave management, and more.

<br>

## Table of Contents
- Features
- Technologies
- Project Setup
- How to Run Tests
- Test Structure
- Contributing

<br>

Features
Automated functional tests for core OrangeHRM modules.
End-to-end testing using Selenium WebDriver.
Written in Java with TestNG as the test framework.
Configurable test environments using Maven.
Page Object Model (POM) for scalable and maintainable tests.
Supports running tests in various browsers (Chrome, Firefox, etc.).
Technologies
Java (programming language)
Selenium WebDriver (browser automation tool)
TestNG (testing framework)
Maven (dependency and build management)
Page Object Model (POM) (for maintainable test code)
Log4j (for logging)
ExtentReports (for generating test reports)
Project Setup
Prerequisites
Java (JDK 8 or higher)
Maven (for dependency management)
ChromeDriver or GeckoDriver (for browser automation)
Git (to clone the repository)
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/orangehrm-automation.git
cd orangehrm-automation
Install dependencies using Maven:

bash
Copy code
mvn clean install
Configure the drivers in the src/main/resources/config.properties:

properties
Copy code
browser=chrome
driverPath=path/to/your/chromedriver
baseUrl=http://orangehrm-demo-6x.orangehrmlive.com/
Update your WebDriver path (if necessary) for your browser (e.g., chromedriver, geckodriver for Firefox).

How to Run Tests
Using Maven
To run all the tests, simply execute the following command in the project root:

bash
mvn test
Using TestNG
You can also run tests directly from your IDE (like Eclipse or IntelliJ) by right-clicking the TestNG.xml file and selecting "Run As -> TestNG Suite".

Running Tests in Different Browsers
To run tests in different browsers, update the browser property in config.properties:

properties
Copy code
browser=firefox
You can choose from supported browsers like chrome, firefox, etc.

Test Structure
The project follows the Page Object Model (POM) design pattern to keep the test scripts clean, organized, and maintainable. Here's the general structure:

bash

src/
│
├── main/
│   └── java/
│       ├── pages/          # Page classes for different modules
│       └── utils/          # Helper utilities and WebDriver management
│
├── test/
│   └── java/
│       ├── tests/          # Test classes (organized by module)
│       └── resources/      # TestNG.xml and config files
Pages: Contains the web page representations using the Page Object Model. Each class corresponds to a different page/module in OrangeHRM.
Tests: Contains the test scripts. Each test class covers specific functionalities of the OrangeHRM.
Reporting
Test results are logged using Log4j and detailed HTML reports are generated using ExtentReports. You can find the reports under:

bash
Copy code
target/extent-reports/
Contributing
Contributions are welcome! If you want to contribute to this project, follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Commit your changes (git commit -m 'Add new feature').
Push to the branch (git push origin feature-branch).
Open a pull request.
Please make sure your code follows the project's coding guidelines and is well-tested before submitting a pull request.
