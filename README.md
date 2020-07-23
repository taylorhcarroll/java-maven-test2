# java-maven-test
## Java environment instructions
I liked the way Visual Studio created C# projects that were plug and play
And wanted a similar functionality with Java and visual studio code. Below 
Is what I've come up with so far.

### Set up Enviornment
Install visual studio
https://code.visualstudio.com/download

Install java jdk and jre 
https://www.oracle.com/java/technologies/javase-downloads.html
get the oracle jdk
https://www.java.com/en/download/
this is for jre

Set environmental variables
    for windows:
    System properties -> Enviornment Variables
        User Variables
            Variable: JAVA_HOME
            Value: C:\Program Files\Java\jdk-14.0.2 (adjust for for jdk version)
        System Variables
            Variable: Path
            Value: C:\Program Files\Java\jre1.8.0_261\bin
            Value: C:\Program Files\Java\jdk-14.0.2\bin

Validate install correctly open vanilla CMD with admin privleges and type:
    java -version
you should get back your java version and not an error

Now type:
    echo %JAVA_HOME%
you should get the path you set


Open visual studio and install Java Extension Pack

Verify Java Language Support for Java(TM) by Red Hat is installed, Maven is installed, and Java Dependency Viewer.

### Create A New Project
While in Visual Studio do CMD+SHIFT+P type:
    Java: Create Java Project

Pick a template 

Input GroupId: must follow naming convention "com.company.projectName"
    **no dashes or other special characters besides ."
Input Artifact ID
    **less critical but whatever you want, lowercase characters ONLY not strange symbols, if third party jar, must take name of jar as distributed
Version: optional
for more info check here:
https://docs.oracle.com/javase/specs/jls/se6/html/packages.html#7.7
https://maven.apache.org/guides/mini/guide-naming-conventions.html

Run program and validate it runs
You can do so in Visual Studio by hitting F5. A terminal should open up and say Hello World! if you chose a quickstart template.
# java-maven-test2
