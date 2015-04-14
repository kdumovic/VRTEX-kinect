# Unreal-Kinect
Unreal 4.6.1 Repo

Kinect Plugin Installation:

NOTE: Current Kinect UE4 plugin only working with 4.6.1 and 4.6.2!

```

1)  Copy the Kinect4Unreal folder into the Plugins folder of your Unreal project.  
2)  Relaunch your Project, the plugin should compile correctly.  If not, double check your version compatability.  
3)  Check in Window->Plugin Manager and scroll down to see if the Kinect plugin installed correctly.  

```

Kinect Plugin Usage:


The full API of commands is available here:

http://opaquemultimedia.com/index.html?pages/k4u.html&k4u

The BP_Robot_Arms blueprint class works by first instantiating the KinectInterface object, and then calling Get Centered Body from it.

From there, the class calls two functions, LHandTracking and RHandTracking.  Both take a Body Number input and then collect joint data from either the L or R hands, scale the vector, rotate it, and set a relative location to the actor objects (Actor SM_spheres).   

Future functionality will include adding other static meshes for hands, adding leap finger support to hands, adapting the actor class to an pawn class, and tweaking movement.  

Currently, the demo has physics enabled with falling space debris to demonstrate the functionality of the robot hands.
