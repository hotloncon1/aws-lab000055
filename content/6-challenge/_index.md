+++
title = "Challenge"
date = 2020
weight = 6
chapter = false
pre = "<b>6. </b>"
+++
#### Challenge
```
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<groupId>devlounge.lambda</groupId>
	<artifactId>flightspecials</artifactId>
	<version>1.0.0</version>
	<packaging>jar</packaging>
	<properties>
	  <maven.compiler.source>1.8</maven.compiler.source>
	  <maven.compiler.target>1.8</maven.compiler.target>
  </properties>
	<build>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.6.0</version>
				<configuration>
					<source>1.8</source>
					<target>1.8</target>
					<encoding>UTF-8</encoding>
					<forceJavacCompilerUse>true</forceJavacCompilerUse>
				</configuration>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-shade-plugin</artifactId>
				<version>3.0.0</version>
				<configuration>
					<createDependencyReducedPom>false</createDependencyReducedPom>
				</configuration>
				<executions>
					<execution>
						<phase>package</phase>
						<goals>
							<goal>shade</goal>
						</goals>
						<configuration>
							<artifactSet>
								<excludes>
									<exclude>com.amazonaws:aws-lambda-java-events</exclude>
									<exclude>com.amazonaws:aws-lambda-java-core</exclude>
								</excludes>
							</artifactSet>
						</configuration>
					</execution>
				</executions>
			</plugin>
		</plugins>
	</build>

	<dependencyManagement>
		<dependencies>
			<dependency>
				<groupId>com.amazonaws</groupId>
				<artifactId>aws-xray-recorder-sdk-bom</artifactId>
				<version>1.1.1</version>
				<type>pom</type>
				<scope>import</scope>
			</dependency>
		</dependencies>
	</dependencyManagement>

	<dependencies>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<version>4.12</version>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<version>8.0.22</version>
		</dependency>
		<dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-lambda-java-events</artifactId>
			<version>1.3.0</version>
		</dependency>
		<dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-lambda-java-core</artifactId>
			<version>1.1.0</version>
		</dependency>

		<dependency>
		  <groupId>org.apache.tomcat</groupId>
		  <artifactId>tomcat-jdbc</artifactId>
		  <version>9.0.39</version>
		</dependency>
		
		<dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-xray-recorder-sdk-core</artifactId>
		</dependency>
		<dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-xray-recorder-sdk-apache-http</artifactId>
		</dependency>
		<dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-xray-recorder-sdk-aws-sdk</artifactId>
		</dependency>
		<dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-xray-recorder-sdk-aws-sdk-instrumentor</artifactId>
		</dependency>
		<dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-xray-recorder-sdk-sql-mysql</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot</artifactId>
			<version>2.0.3.RELEASE</version>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-autoconfigure</artifactId>
			<version>2.0.3.RELEASE</version>
		</dependency>
		<dependency>
    		<groupId>org.json</groupId>
    		<artifactId>json</artifactId>
    		<version>20180130</version>
		</dependency>
		<dependency>
			<groupId>com.amazonaws.serverless</groupId>
			<artifactId>aws-serverless-java-container-core</artifactId>
			<version>1.1.3</version>
		</dependency>
		<dependency>
			<groupId>org.junit.jupiter</groupId>
			<artifactId>junit-jupiter-api</artifactId>
			<version>5.2.0</version>
		</dependency>
	</dependencies>
</project>
```


As an optional task, you are challenged with implementing active tracing using automation for the functions deployed using the AWS CLI and CodeStar. We are not going to give you all the answers! But to help you on your journey, check out the [**AWS::Lambda::Function**](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html) tCloudFormation documentation, and [**AWS SAM**](https://github.com/awslabs/serverless-application-model/blob/master/versions/2016-10-31.md) documentation.

When you have fully implemented tracing for the Lambda functions, you will see the tracing segments on the AWS X-ray console. Trigger the execution of the various lambda functions using the TravelBuddy SPA web page, and you will see results such as:

![Challenge](/images/6-challenge/challenge-001.png?featherlight=false&width=90pc)