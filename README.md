# Rest-Assured-Data-Driven-Framework

This template will help you to have a data driven framework with Rest Assured. Here we are using apache POI to read data from a excel file. We have a seperate class to read the data from an external file and we can call this call in your test script, so that we can have a more granular test project.

To read data from an excel file we need Apache POI maven dependency

        <dependency>
            <groupId>org.apache.poi</groupId>
            <artifactId>poi-ooxml</artifactId>
            <version>3.17</version>
        </dependency>
        <dependency>
            <groupId>org.apache.poi</groupId>
            <artifactId>poi</artifactId>
            <version>3.17</version>
        </dependency>

We have used TestNg here, so that we can have the luxury to tagging out test cases/methods. TestNg dependency is mentioned below

            <dependency>
                <groupId>org.testng</groupId>
                <artifactId>testng</artifactId>
                <version>7.3.0</version>
                <scope>test</scope>
            </dependency>

And also, we have used the JsonSimple dependecy as well. JSON simple is a simple Java based toolkit for JSON. You can use JSON.simple to encode or decode JSON data. Therefore, in order to assert the json response in a more efficent fashion we have used this as well.

And at last we have the main dependency of this template i.e, rest-assured dependency.

        <dependency>
            <groupId>io.rest-assured</groupId>
            <artifactId>rest-assured</artifactId>
            <version>4.3.3</version>
            <scope>test</scope>
        </dependency>

# Why we need a Data Driven Framework? 

These are the main keypoints for having an data driven approach in our testing framework.

1. Allows to test application with multiple sets of data values during Regression testing.
2. Test data and verification data can be organized in just one file, and it is separate from the test case logic.
3. Data-driven testing can perform any phase of the development.
4. Allows developers and testers to have clear separation for the logic of their test cases/scripts from the test data.
5. Any changes in the test script do not have any sideffect on the test data.
6. To create an individual test for each data set is a lengthy and time-consuming process. Data Driven Testing framework resolves this issue by keeping the data separate from Functional tests.

In order to run the test, we just have to go into the directory ../Rest-Assured-Data-Driven-Framework/DataDrivenFramework-RestAssured and run the command

mvn -Dtest=ReadFile test

But first export the data file path before executing the tests

export filePath='path_to_your_data_file'




