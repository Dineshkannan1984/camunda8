Camunda Platform - Submission for Consultant Role

This Repository contains a  simple Camunda Client App using  Camunda 8, where the process will be start using Rest API

Once the process starts , the user flow will be triggered and will be prompted for selection of  random picture of a cat, a dog, or a bear of user choice

On selection the selected picture will be stored to H2 Database

The project was developed using Spring Boot 3.X + Java 17  and Helm file attached for deployment

Minimal Spring Boot sample app.

Requirements
For building and running the application you need:

JDK 1.8
Maven 3
Running the application locally
There are several ways to run a Spring Boot application on your local machine. One way is to execute the main method in the de.codecentric.springbootsample.Application class from your IDE.

Alternatively you can use the Spring Boot Maven plugin like so:

mvn spring-boot:run
Deploying the application to OpenShift
The easiest way to deploy the sample application to OpenShift is to use the OpenShift CLI:

oc new-app codecentric/springboot-maven3-centos~https://github.com/codecentric/springboot-sample-app
This will create:

An ImageStream called "springboot-maven3-centos"
An ImageStream called "springboot-sample-app"
A BuildConfig called "springboot-sample-app"
DeploymentConfig called "springboot-sample-app"
Service called "springboot-sample-app"
If you want to access the app from outside your OpenShift installation, you have to expose the springboot-sample-app service:

oc expose springboot-sample-app --hostname=www.example.com
Copyright
Released under the Apache License 2.0. See the LICENSE file.