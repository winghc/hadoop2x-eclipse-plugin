hadoop2x-eclipse-plugin
=======================

eclipse plugin for hadoop  2.5.1
 

How to build
----------------------------------------

  $cd src/contrib/eclipse-plugin 

  $ant jar -Dversion=2.5.1 -Declipse.home=/opt/eclipse -Dhadoop.home=/usr/local/hadoop

final jar will be genrated at directory 

  $root/build/contrib/eclipse-plugin/hadoop-eclipse-plugin-2.5.1.jar

options required
--------------------------------------
  eclipse.home: path of eclipse home 

  hadoop.home: path of hadoop 2.x home
 

How to debug
--------------------------------------
  start eclipse with debug parameter:  

    /opt/eclipse/eclipse -clean -consolelog -debug
    

Note: compile issues resolve: 
--------------------------------------
1. Check the version that you want to cimpile with, e.g: hadoop-eclipse-plugin-2.4.0.jar 
2. Find the jars version at the file build.xml in the node: <attribute name="Bundle-ClassPath" .... 
   and add the folder named "lib" at the path, e.g: ${hadoop2x-eclipse-plugin-master}\src\contrib\eclipse-plugin\lib
   also add the needed jar files to this folder which this node needed, and the version written in the file
   ${hadoop2x-eclipse-plugin-master}\ivy\libraries.properties, make the version is correct.
3. Then run the command: ant jar -Dversion=2.4.0 -Declipse.home=/opt/eclipse -Dhadoop.home=/usr/share/hadoop
