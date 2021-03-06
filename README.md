# Guide To Create Millenium Falcon Augmented Reality Application

This is a repo that has the assets and instructions to build the AR Millenium Falcon Application built at a talk for Tech Elevator 1-24-18.

Instructions:

-Download and install Unity( These instructions were made for version 2017.3 : https://unity3d.com/

-Make sure to include the vuforia component
![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/vuforiaInstallation%200.png)

-Download the image you want to use as a marker. I used a dollar bill.

-Download the 3d model you would like to use. The Millenium Falcon model I used can be found here: https://free3d.com/3d-model/puo-4036-1699.html

-Sign Up For Vuforia: https://developer.vuforia.com/

-Under License Manager, create a license key. Save this for use later.

-Under Target Manager, on Vuforia's website click "Add Database". Create a database and select type "Device".

-Open the newly created database and click "Add Target".

-For type select "Singe Image" upload your image give it a width of 5 and give it a name and click add.

-Select "Download Database" and save the file for Unity Editor.

-Open Unity and create a new project.

-Change build setting to iOS or Android
![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/changeBuildSettings.gif)

-Under GameObjects > Vuforia creates an ARCamera. Delete the Main Camera

![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/addArCamera.gif)

-Drag in/Import your downloaded image marker database

![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/importImageMarkerDatabase.gif)

-In Build Setting>Player Settings under XR settings enable the project to use Vuforia
![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/changeXrSettings.gif)

-Select ARCamera and in Vuforia Behaviour select Open Vuforia configuration.

-Add your app license key

-Under databases select to load your image target database and activate

-Add Gameobject>Vuforia>Image	

-In database Select image target object and from the dropdown select the correct database and make sure the image target is correct

![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/addKeyAndDatabse.gif)
-Add Gameobject>Vuforia>Image	

-In database Select image target object and from the dropdown select the correct database and make sure the image target is correct

![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/addImageTarget.gif)
-Upload 3d model and place it inside image target and position above the marker

-Make sure it is INSIDE (AKA a child of) the image target. GIFs dont show this until later on.
![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/upload%203d%20model.gif)

-Test to make sure image tracking is working
![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/confirmTrackingIsWorking.gif)

-Assests>ImportPackages>CrossPlatformInput

-Drag in Standard Assets>CrossPlatformInput>Prefabs>MobileSingleStickControl into the Hierarchy

-Remove Jump button

-Make Joystick Movement Range 50
![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/addjoystick.gif)

-Go to 3D model  click Add component in the inspector and add rigidBody Component

-Uncheck use gravity

-Add an Audiosource component to the Millenium Falcon Model

-Add the audio file to unity and drag it in to the audioClip selector on millenium falcon AudioSource component

-Uncheck play on awake.

![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/rbAndAudio.gif)

-Add a new script component named "MilleniumFalconMovement" on Millenium Falcon Model

-Write the script for movement and audio. See attached script
![alt text](https://github.com/nstaab1/ARPresentationAppWalkThrough/blob/master/screenshots/addScript.gif)

-Make sure everything builds correctly



-Build To Phone

^I will not write out how to get the application on your phone just google for directions on building to iOS or Android from Unity.


Thank You For Following along with this tutorial. 

Feel free to add us on LinkedIn: 
https://www.linkedin.com/in/nathanstaab/
https://www.linkedin.com/in/martyaddante/

For business inquiries email me here: nstaab443@gmail.com



