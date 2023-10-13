# Switch Between Java Versions

To [run Voyant-Tools on my local machine](https://github.com/voyanttools/VoyantServer), rather than the [web version](https://voyant-tools.org/), I need to be running a previous version of Java. Below are the steps I take to switch between versions. I'm running OSX Monterey 12.4. 

- Open terminal at the folder level where my voyant-tools server is located.
- Check the Java version with `java -version`
- Run the following command: ``` - export JAVA_HOME=`/usr/libexec/java_home -v 1.8` ```
- Check the Java version again to confirm it moved to 1.8
- Run ```java -jar VoyantServer.jar``` to open Voyant-tools Server
- 