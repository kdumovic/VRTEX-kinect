# Unreal-Kinect
Unreal 4.6.1 Repo

Kinect Plugin Installation:

NOTE: Current Kinect UE4 plugin only working with 4.6.1 and 4.6.2!

1)  Copy the Kinect4Unreal folder into the Plugins folder of your Unreal project.  
2)  Relaunch your Project, the plugin should compile correctly.  If not, double check your version compatability.  
3)  Check in Window->Plugin Manager and scroll down to see if the Kinect plugin installed correctly.  

Kinect Plugin Usage:

The full API of commands is available here:

http://opaquemultimedia.com/index.html?pages/k4u.html&k4u

A sample blueprint BP_Introduction_Bones3D.uasset shows how bone joint recognition works:

This class uses the "Get Hand State As Execution" function:

Inputs: 

Target, should go to the Kienct Interface component created

Hand, Enumerated Hand (Left or Right) if you want, or else it will use either detected

Body Number, Same Enumerated value, Kinect can track up to 8 body numbers

Outputs: 

Unknown: Kinect is not confident enough to tell

Not Tracked:  Kinect is not tracking any hands

Open:  One hand is in an open state

Closed:  One hand is in a closed state

Lasso:  Yee haw cowboy, them be a lasso in your hands!

Each of these outputs can lead to event logic, for example, I created OSC Send events from both the Open and Closed states.
