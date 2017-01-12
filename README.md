HyperSpeedCube
-------------------------------------
[Asset Store Link](http://u3d.as/HaD)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

Contact  
-------------------------------------
Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.net/contact](http://justingarza.net/contact/)
  
Description/Features
-------------------------------------
HyperSpeedCube is a fast pace game that will pushes the boundaries of your speed and reaction.* Unique fast paced game!
* 7 Awesome Levels!
* Native share feature!
* Unity Ads!
* Over 1,500 Icons!
* ShockWave screen effect!
Terms of Use
-------------------------------------
You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

Table of Contents 
-------------------------------------
1. GameFlow 
	* Start
	* OutOfCubes
	* MainMenu
	* Info
	* Levels ##
2. Systems/Effects
	* Lives
	* PageR
	* Audio (Music/Sound)
	* SceneSwitchAnimator
	* Native Sharing
	* Level Creation/IntersectionEditor 	 
3. Scripts   


  
GameFlow
-------------------------------------
![Imgur](http://i.imgur.com/0FKukowm.png)

**Start**  
While starting the app the user will first load the OutOfCubes Scene.

**OutOfCubes**  
The User will exit this screne when:  
They have more than 0 Lives(Cubes)  
or They have watched an Ad (thus increasing Lives/Cubes)
or They have waited 10 minues (thus increasing Lives/Cubes)

**MainMenu**  
This scene allows the user to pick levels, or change settings.

**Info**  
This scene displays information about the Game.
(Please keep my name here).

**Levels ##**  
These are the Levels
Exiting a Level will take the user back to the MainMenu.
Running out of Lives will force the player to go to the OutOfCubes Scene.


Systems/Effects 
-------------------------------------
**Lives**  
Lives are stored as an Int in PlayerPrefs.
When the user runs out of lives they will be forced to go to the OutOfCubes Scene. There they must watch an Ad or wait to gain more Lives/Cubes.

**PageR**
This is used in the MainMenu Scene.  
For more Info read ~Assets/HyperSpeedCube/PageR/README.pdf

**Audio (Music/Sound)**  
MusicManager and SoundManager are two Objects that are never destroyed.
They are used to play Music or a Sound without the need for each object to have it's own AudioSource Component, and this allows us to play sounds while the scene is switching. 
Read MusicManager.cs and SoundManager.cs for more info.

**SceneSwitchAnimator**  
This GameObject will allow us to have a nice scene animation while changing scenes.

**Native Sharing**  
This is an OpenSourced asset that can be found at...  
https://github.com/ChrisMaire/unity-native-sharing

**Level Creation/IntersectionEditor**  
The following are the steps for creating a new Level.  

1. Make a copy of "Level00_Template" and rename it as needed.
2. Open the new Scene.
3. Disable all objects except for "GridObjects" and it's child objects.
4. Use the Scene View to select objects and intersectionType to whatever you want.
	* Make sure there is at least 1 Point/Gem.
5. Enable the objects (see step 3)
6. Move the player object to a good Spot
	* Make sure they are aligned with the Objects
	* Change the initDirection (of the player), if needed
7. Save the Scene.
8. Change the MainMenu so that the user can access the new Level.



Scripts 
-------------------------------------
Below is a list of the scripts that make this game work, along with a breif description of what they do.

###~Assets/HyperSpeedCube/Scripts/###

**AnimateGroundMaterial.cs**  
Used to animate the GroundMaterial.

**CameraFollow.cs**  
Moves the camera to follow the player, during the LevelScenes

**CountDown.cs**  
Performs a countdown before the game starts, and when the player resumes game after pausing

**ControlButtons.cs**  
This script matches a down press on a button to the player's action

**CreateGrid.cs**  
An editor only script that easily creates a grid of objects

**DontDestroy.cs**  
This script will allow an object to live on after scene transition.

**GameManager.cs**  
This script manages game states during a LevelScene.
GameManagerStates (GMStates) include INTRO, PLAYING, PAUSE, WIN, GAMEOVER.

**GoToScene.cs**  
This Script can be assigned to buttons to Switch Scenes.

**LRButtons.cs**  
Used to flip the pages Left and Right

**IntersectionEditor.cs**  
This script will allow you to easily edit each intersection in the level.
Change from Null, Point, Death, or Bounce. 

**ObjectPool.cs**  
A pool of objects that can be reused.

**MusicManager.cs**  
This script is used to manage the music.

**OutOfLives.cs**  
This Script controls most of what happens in the OutOfCube/OutOfLives Scene

**perimeterDetect.cs**  
Detects where Points/Gems are surrounded by RedObjects(Death) in a square pattern and removes them.

**Player.cs**  
A State Machine that controls the player.
more about state machines:
https://unity3d.com/learn/tutorials/topics/scripting/using-interfaces-make-state-machine-ai

**PlayerPrefsBool.cs**  
Contains methods for storing bools in the PlayerPrefs.
Note: stores 0 and 1 as int, but converts it to a bool on return

**PlayerPrefsColor.cs**  
This Script adds color saving functions to PlayerPrefs

**PlayerRenderer.cs**  
Renders the player in multiple locations, for seemless looping

**PlaySound.cs**  
This script is used to play a sound

**PlayerShadow.cs**  
Controls the Player's Shadow

**Points.cs**  
Manages the points.

**PoolManager.cs**  
This script manages pools of objects
Spawning and Recycling.

**ReColor_Level.cs**  
Sets the Color for the Level when it starts.
The Colors are based on the colors on the MainMenu.

**ReColor_MainMenu.cs**  
Updates the Colors on the MainMenu, and sets the colors for the Levels.

**SetMenuTxt.cs**  
Sets the Text in the Menu.

**SceneMusic.cs**  
Changes the music track on Start

**SetUp.cs**  
Creates GameObjects on Awake...but don't create them if they exists.

**ShareButton.cs**  
Used to Share this app

**SoundManager.cs**  
This script is used to manage the Sounds.

**ShowLives.cs**  
Show number of Lives in the top right corner of the MainMenu

**Timer.cs**  
Timer used during play

**VolumeSwitch.cs**  
This Script can be assigned to a toggle to control Music or Sound

**WinFlag.cs**  
Shows if you win the level.

###~Assets/HyperSpeedCube/SceneSwitchAnimator/Scripts/### 

**SceneSwitchAnimator.cs**  
This script manages the animation before and after the scene switchs.

###~Assets/HyperSpeedCube/ShockWave/Scripts/### 

**ShockWave.cs**  
Creates and Manages the ShockWave

