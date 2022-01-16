Shimeji-ee:

Shimeji-ee is a Windows desktop mascot that freely wanders and plays around the screen. The mascot is very configurable; its actions are defined through xml and its animations/images can be (painstakingly) customized. Shimeji was originally created by Yuki Yamada of Group Finity (http://www.group-finity.com/Shimeji/). Moreover, Kilkakon (http://kilkakon.com/shimeji) and other members of the community, branched the original Shimeji project to not only translate the program/source to English, but added additional enhancements to Shimeji. Currently, Aja Khanal, Soran-i and PashaRah are cleaning up/updating all the extra unnecessary code, renovating GUIs, and plan to add modern assistive features to add viability to the simple fun program.

==== Contents ====

Our Intentions
Requirements
How to Start
Basic Configuration
Advanced Configuration
How to Quit
How to Uninstall
Source
Library
Troubleshooting
Additional Note

==== Our Story/Intentions ====

We observed that several of the capabilities were broken or missing since the code had not been updated in a long time. We decided as a group to rebuild various sections of the code in order to breathe new life into virtual pets and virtual assistants. Assistants like Peedy the Parrot, Clippy, and BonziBuddy, we believe, had a lot going for them. We reckon Shimeji-ee might add some more fun to your desktop, especially in this day and age, when Amazon Alexa, Google Assistant, and Siri are all the trend.

==== Requirements ====

Windows Vista or higher
Java 8
Around 256mb of free ram

==== How to Start ====

Double Click the Shimeji-ee.jar file

Right click the tray icon for general options.

Right click a Shimeji to open the command menu.

For a video tutorial on how to get Shimeji running: https://www.youtube.com/watch?v=S7fPCGh5xxo

==== Basic Configuration ====

If you want multiple Shimeji types, you must have multiple image sets. Basically, you put different folders with the correct Shimeji images under the img directory.

For example, if you want to add, say, a new Batman Shimeji:

Create an img/Batman folder.
You must have an image set that mimics the contents of img/Shimeji. Create and put new versions of shime1.png - shime46.png (with Batman images of course) in the img/Batman folder. The filenames must be the same as the img/Shimeji files. Refer to img/Shimeji for the proper character positions.
Start Shimeji-ee. Now Shimeji and Batman will drop. Right click Batman to perform Batman specific options. Adding "Call Shimeji" from the tray icon will randomly create/add either Shimeji or Batman.
When Shimeji-ee starts, one Shimeji for every image set in the img folder will be created. If you have too many image sets, a lot of your computer's memory will be used... so be careful. 

Shimeji-ee will ignore all the image sets that are in the img/unused folder, so you can hide image sets in there. There is also a tool, Image Set Chooser, that will let you select image sets at run time. It remembers previous options via the conf/settings.properties file. Don't choose too many at once.

For more information, read through the configuration files in conf/. Most options are somewhat complicated, but it's not too hard to limit the total number of Shimeji or to turn off certain behaviors (hint: set frequency to 0.)

==== Advanced Configuration ====

All configuration files are located in the conf folders. In general, none of these should need to be touched.

The logging.properties file defines how logging errors are done. The actions.xml file specifies the different actions Shimeji can do. When listing images, only include the file name. More detail on this file will hopefully be added later. The behaviors.xml file specifies when Shimeji performs each action. More detail on this file will /hopefully be added later. The settings.properties file details which Shimeji are active as well as the windows with which they can interact. These settings can be changed using the program itself.

Each type of Shimeji is configured through:

An image set. This is located in img/[NAME]. The image set must contain all image files specified in the actions file.
An actions file. Unless img/[NAME]/conf/actions.xml or conf/[NAME]/actions.xml exists, conf/actions.xml will be used.
A behaviors file. Unless img/[NAME]/conf/behaviors.xml or conf/[NAME]/behaviors.xml exists, conf/behaviors.xml will be used.
Shimeji-ee will ignore all the image sets that are in the img/unused folder, so you can hide image sets in there. There is also a tool, Image Set Chooser, that will let you select image sets at run time. It remembers previous options via the ActiveShimeji file. Don't choose too many at once.

The Image Set Chooser looks for the shime1.png image. If it's not found, no image set preview will be shown. Even if you're not using an image named shime1.png in your image set, you should include one for the Image Set Chooser's sake.

Editing an existing configuration is fairly straightforward. But writing a brand new configuration file is very time consuming and requires a lot of trial and error. Hopefully someone will write a guide for it someday, but until then, you'll have to look at the existing conf files to figure it out. Basically, for every Behavior, there must be a corresponding action. Actions and Behaviors can be a sequence of other actions or behaviors.

The following actions must be present for the actions.xml to be valid:

ChaseMouse Fall Dragged Thrown

The following behaviors must be present for the behaviors.xml to be valid:

ChaseMouse Fall Dragged Thrown

The icon used for the system tray is img/icon.png

==== How to Quit ====

Right-click the tray icon of Shimeji, Select "Dismiss All"

==== How to Uninstall ====

Delete the unzipped folder.

==== Source ====

Programmers may feel free to use the source. The Shimeji-ee source is under the New BSD license. Follow the zlib/libpng licenses.

==== Library ====

lib / jna.jar and lib / examples.jar of the JNA library. JNA follows the LGPL. lib / AbsoluteLayout.jar from Netbeans.

==== Troubleshooting ====

For a video FAQ, if you encounter problems: 
https://www.youtube.com/watch?v=A1y9C1Vbn6Q

You can also join the Discord group: https://discord.gg/dcJGAn3

Expect some loading time when launching Shimeji-ee. To determine if you have a memory problem, move all but one picture set from the img folder to the img/unused folder. If Shimeji is running out of memory, change "-Xmx1000m'' to a larger value in Shimeiji-ee.bat.

If the Shimeji-ee icon appears, but no Shimeji appear:

Make sure you have the newest version of Shimeji-ee.
Make sure you only have image set folders in your img directory.
Make sure you have Java on your system.
If you're somewhat computer savvy, you can try running Shimeji-ee from the command line. Navigate to the Shimeji-ee directory and run this command: "C:\Program Files (x86)\Java\jre6\bin\java" -jar Shimeji-ee.jar
Try checking the log (ShimejiLogX.log) for errors. If you find a bug (which is very likely), post it up on the Shimeji-ee homepage in the issues section.

==== Additional Note ====

It's essential to ensure you acquire shimeji-ee from a viable source. As individuals can code shimeji-ee to perform undesirable activities since it is an open source application. If possible download it from https://github.com/AjaKhanal/Crewmate.

