# wp-oss-parent-pom
Parent POM for open source com.washingtonpost artifacts.

This POM contains common build configurations required for releasing source to Maven Central and Sonatype's STAGING Nexus servers.

To use this in your washingtonpost.com project, follow the localhost setup [instructions on the Wiki](http://confluence.washpost.com/display/GE/How-To%3A+Contribute+open+source+code).

## Usage

To inherit from this POM, just add it as your artifact's parent:

```
    <parent>
        <groupId>com.washingtonpost</groupId>
        <artifactId>wp-oss-parent-pom</artifactId>
        <version>...</version>
    </parent>
```

You'll get standard maven dependency plugin management and it'll enable you to release your application to Maven Central with 
```
mvn -Prelease-opensource release:prepare
mvn -Prelease-opensource release:perform
```