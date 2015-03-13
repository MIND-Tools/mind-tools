# mind-tools
Maven pom project to build a full integrated release of MIND tools - compiler / doc / plugins

# Global prerequisites

* Maven 3.0.5
* JDK >= 6
* GCC
* G++
* https://github.com/MIND-Tools/mind-tools-release-scripts
* https://github.com/MIND-Tools/mind-tools-release-manifest

This build must be ran after all repositories have been cloned in the right folders.

This preparation step is usually done thanks to the "mind-tools-create-workspace" script (called first by mind-tools-install-release-full-linux.sh), using the Android Repo (Python-based) tool to clone all the repositories and checkout the right branches, according to the manifest contained in the repository mentioned previously.

# Local build

1. `mvn clean install -f ./mind-compiler/pom.xml --projects org.ow2.mind:mind-compiler`
2. `mvn clean install`

Those steps are those used in the "mind-tools-install-release" script  (called first by mind-tools-install-release-full-linux.sh, after the "mind-tools-create-workspace").

# Continuous integration

## Note

Up to this day we need to first install the "abstract" mind-compiler pom information to the local cache prior to really building the modules, because of a project construction order issue.

## Build

1. `mvn -s path/to/settings.xml clean install -f ./mind-compiler/pom.xml --projects org.ow2.mind:mind-compiler`
2. `mvn -s path/to/settings.xml clean install`
3. TODO: mvn deploy with configuration
