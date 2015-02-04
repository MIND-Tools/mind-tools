# mind-tools
Maven pom project to build a full integrated release of MIND tools - compiler / doc / plugins

# Global prerequisites

* Maven 3.0.5
* https://github.com/MIND-Tools/mind-tools-release-scripts
* https://github.com/MIND-Tools/mind-tools-release-manifest

# Local build

1. `mvn clean install -f ./mind-compiler/pom.xml --projects org.ow2.mind:mind-compiler`
2. `mvn clean install`

# Continuous integration

## Note

Up to this day we need to first install the "abstract" mind-compiler pom information to the local cache prior to really building the modules, because of a project construction order issue.

## Build

1. `mvn -s path/to/settings.xml clean install -f ./mind-compiler/pom.xml --projects org.ow2.mind:mind-compiler`
2. `mvn -s path/to/settings.xml clean install`
3. TODO: mvn deploy with configuration
