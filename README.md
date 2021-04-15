# tybatest
TYBA TEST repository


[![gradle](https://img.shields.io/badge/gradle-v4.9.X-yellow.svg)](https://gradle.org/install/)
[![maven](https://img.shields.io/badge/maven-v3.6.X-red.svg)](https://maven.apache.org/)


>A Gradle & Maven project to test TYBA, Java, Serenity &&  Cucumber. `:wq`
>

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](http://git-scm.com/)
* [Gradle](https://gradle.org)
* [Maven](https://maven.apache.org/)
* [Java](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)


## Installation

We use [Gradle](http://www.gradle.org), a cross-platform build automation tool that help with our full development flow. 
If you prefer [install Gradle](http://www.gradle.org/installation) or use a [Gradle wrapper](http://www.gradle.org/docs/current/userguide/gradle_wrapper.html) inside this project.

* ´git clone https://github.com/SergioAG666/tybatest.git` this repository
* change into the new directory `cd tybatest`

##  Executing the tests

the parameter **-Denvironment** can to take values like: 

   - pro
   
By default, the tests will run using Chrome browser.

For Gradle:
```bash
./gradlew clean test aggregate -Denvironment=pro
```
For Maven: 
```bash
 mvn clean verify -Denvironment=pro 
```

with Maven and other webdriver (browser)

```bash
 mvn clean verify -Denvironment=stg  -Dwebdriver.driver=firefox
```
The test results will be recorded in the `target/site/serenity` directory.

## Simplified WebDriver configuration and other Serenity extras
The sample projects both use some Serenity features which make configuring the tests easier. In particular, Serenity uses the `serenity.conf` file in the `src/test/resources` directory to configure test execution options.  



### The project directory structure
The project has build scripts for both Maven and Gradle, and follows the standard directory structure used in most Serenity projects:
```Gherkin
src
  + test                             |
    + java                           | Test runners and supporting code
        + co.bpop.ahorro.qa          | Package base
          + features                 | Features set
            + {feature_name}         | Feature name
            + steps                  | Utility class for definition steps
            + {feature_name}.java    | Definition class 
            + Runner.java            | Main class
          + questions
          + tasks
          + user_interface           | 
          + utils                    | General utility class
    + resources                      |
      + features                     | Feature files
          {feature_name}.feature     | Feature file specific
      serenity.conf                  | Config file for Serenity
      stg.properties
serenity.properties                  | General properties Serenity
```


## Install webdrive local

```bash
brew tap homebrew/cask && brew cask install chromedriver

```

## Want to learn more?
For more information about Serenity BDD, you can read the [**Serenity BDD Book**](https://serenity-bdd.github.io/theserenitybook/latest/index.html), the official online Serenity documentation source. Other sources include:
* **[Byte-sized Serenity BDD](https://www.youtube.com/channel/UCav6-dPEUiLbnu-rgpy7_bw/featured)** - tips and tricks about Serenity BDD
* [**Serenity BDD Blog**](https://johnfergusonsmart.com/category/serenity-bdd/) - regular articles about Serenity BDD
* [**The Serenity BDD Dojo**](https://serenitydojo.teachable.com) - Online training on Serenity BDD and on test automation and BDD in general. 

