hadoop2x-eclipse-plugin
=======================

eclipse plugin for hadoop 2.2.0
 

How to build
----------------------------------------

  $cd src/contrib/eclipse-plugin 

  $ant jar -Dversion=2.2.0 -Declipse.home=/opt/eclipse -Dhadoop.home=/usr/share/hadoop

final jar will be genrated at directory 

  $root/build/contrib/eclipse-plugin/hadoop-eclipse-plugin-2.2.0.jar

options required
--------------------------------------
  eclipse.home: path of eclipse home 

  hadoop.home: path of hadoop 2.x home
 

How to debug
--------------------------------------
  start eclipse with debug parameter:  

    /opt/eclipse/eclipse -clean -consolelog -debug

