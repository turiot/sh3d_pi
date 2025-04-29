Experiments SweetHome3D on raspberry pi 5

Prerequisites
-------------
change pi configuration from wayland to X11

install java (17+)

Package Installation
--------------------
unzip https://github.com/turiot/sh3d_pi/releases/download/1.0/SweetHome3D-7.5.zip where you want

sh SweetHome3D

Changes made
------------
* from orginal sh3d distribution (https://sourceforge.net/projects/sweethome3d/files/SweetHome3D/SweetHome3D-7.5/SweetHome3D-7.5-portable.7z/download)
  
* removed :

 runtime

 lib/java3d-1.6

 lib/j3dcore.jar

 lib/j3dutils.jar

 lib/libj3dcore.so

 lib/vecmath.jar

* added (from https://github.com/processing/processing4/releases)

lib/jogamp :

  processing-4.3-linux-arm64.tgz/processing-4.3/core/library/core.jar
  
  processing-4.3-linux-arm64.tgz/processing-4.3/core/library/gluegen-rt.jar
  
  processing-4.3-linux-arm64.tgz/processing-4.3/core/library/jogl-all.jar
  
  lib/java3d-1.6/j3dcore.jar
  
  lib/java3d-1.6/j3dutils.jar
  
  lib/java3d-1.6/vecmath.jar
  
natives/linux-aarch64 :

  processing-4.3-linux-arm64.tgz/processing-4.3/core/library/linux-aarch64/*
  
* added marlin (from https://github.com/bourgesl/marlin-renderer)
  
* launcher updated consequently

Notes
-----
* java 3d (jogl) on raspberry works
  
  processing and "art of illusion" also
  
* opengl renderer for 2d doesn't work (driver is incompatible)
  
  but marlin give a very efficient boost
  
  you can also deactivate grid and rulers
  
* yafaray : need to build on aarch64 (sunflow works)
  
* wayland is not java swing friendly

  overclocking is an option
  
  rockchip test welcome

Thanks
------
shd3 team (Emmanuel Puybaret)

jogamp team (for jogl)

processing team (for packaing jogamp)

marlin developper (Laurent Bourgès)

raspberry pi os team (and video driver devs)
