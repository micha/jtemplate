JTemplate
=========

JTemplate is a simple java project skeleton. Use it to start out new java
projects without making a big deal out of it. There are no dependencies other
than [java][] and [ant][], and there is no framework or IDE needed. Good for
if you don't use Eclipse or Netbeans or whatever.

[java]:       http://sun.java.com/      "Java"
[ant]:        http://ant.apache.org/    "ant"

Quickstart
----------

1.  Create a github repo.

2.  From the new repo do `git pull git://github.com/micha/jtemplate.git master`.

3.  Edit the _build.xml_ file to your liking.  The first few properties
    are clearly marked, and are expected to be set for your specific
    project.

4.  Run `ant init`.  This makes you a _/src_ tree with a Main class stub and
    the _resources/_, _lib/_, and _doc/_ directories for your resource files,
    external jarfile dependencies, and project documentation.

5.  Run `ant install`. This creates the jar file and wrapper script in the
    _dist/_ directory and installs the wrapper in a bin directory in your
    path (or wherever you specify at the prompt).

5.  Done. The wrapper script is named the same as your project name, so you
    can run the Java app in the terminal.

Ant targets you might use from here on out (remember ant -projecthelp): 

+ 'install'
+ 'clean'
+ 'dist'
+ 'jar'
+ 'compile'
+ 'javadoc'

Directories
-----------
    
+ __docs:__ Project documentation. API javadocs will be written to _docs/api/_ 
  directory. You can include anything you want here (documentation for 
  dependencies, etc).  

+ __lib:__ Jar files to be incorporated into the distribution jar file.

+ __resources:__ Resources to be included in the distribution jar file.  They 
  will be added to the jar with a path relative to this directory, i.e., 
  resources/foo/bar.jpg will be accessed in java as "foo/bar.jpg".

+ __src:__ Java source files go here.

Files
-----

+ __dist/<i>projectname</i>.zip__ Zipfile containing jar file and Application 
  launcher wrapper script.

+ __resources/version__ Contains the app version number. This is accessible
  as a jarfile resource from your app, if you want to implement a *--version*
  command line option or something.
