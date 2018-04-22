BRWAP Bus Audio
This guide is intended to introduce you to the development of the audio app that runs on an Android tablet for the bus audio system. You can create the audio .WAV files in any recording device. Determine which sequence the content needs to be based on where the animals are placed in the park. At this time you will use a basic HTML editor to create the “web page” that will be compiled and loaded onto the Android tablet. Once these are complete, you will use the Cordova Apache development software to compile the code and create the app that is then transmitted to the tablets for use.
Web App
This is the part where your application code resides. The application itself is implemented as a web page, by default a local file named index.html, that references CSS, JavaScript, images, media files, or other resources are necessary for it to run. The app executes in a WebView within the native application wrapper, which you distribute to the tablet.
This container has a very crucial file - config.xml file that provides information about the app and specifies parameters affecting how it works, such as whether it responds to orientation shifts.
Audio file creation
The audio files need to be created using the narrative that you want the audience to hear. Talk about the characteristics, origin, habitat, life cycle, and if desired the length of time the animal has been at BRWAP. Each animal will have a unique audio file that will be placed in a sequence each year. Personally I like to use Audacity on a Windows computer to allow for minor mixing of music with the narrative.
Web Page creation
The web page is a very basic HTML file that contains Left justification, Right justification, and Center justification to locate the button for the animal on the tablet. Each animal will have a button that will be pressed for the narrative to be played throughout the bus speaker system. While this portion is not complex, it is very detail oriented. When creating this web page concentration is needed in order to maintain the code syntax needed for proper display on the device.
We will use a simple WYSIWYG editor – (What You See Is What You Get) is a very basic editor for HTML files. The template was created and we will just modify each year based on the sequence the animals are within the park.
App Compile
The App is compiled using Cordova Apache software. This is the only part that is specific to the machine that has the software installed. Currently there are two computers with this capability. The computer in the gift shop office and Dawn’s personal laptop. If you need to configure a computer for this, it will take about 4 hours. Please follow the instructions at this YouTube video (and the next in the series): https://www.youtube.com/watch?v=LLX2FEg0TjU
Please continue to the second video in the series as you will also need GIT.
Install the next tool from this path: https://code.google.com/archive/p/winant/downloads
This is the link direct to the download: https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/winant/winant-install-v7.exe
Update the path: C:\Program Files (x86)\Android\android-sdk\tools\
Once these steps are complete you should be ok to develop and compile the android app.
I like to use the KompoZer tool to edit the HTML files as it shows both the graphic version and the Source code – typically I use the Split mode so I can see both. The person that created the video uses Notepad++ to edit HTML files.
https://downloads.sourceforge.net/project/kompozer/current/0.7.10/kompozer-0.7.10-win32.zip?r=http%3A%2F%2Fwww.kompozer.net%2F&ts=1494760307&use_mirror=managedway
NOTE: If you are doing the steps in the video where he asks you to load the android platform, change it to: ionic cordova platform add android
As the cordova is specific and has changed since his video.
Open CMD prompt then type:
ionic start SafariAudio blank
Install Gradle https://services.gradle.org/distributions/gradle-3.5-all.zip This replaced ANT

cd Sa <TAB><ENTER>
ionic cordova platform add android
ionic cordova build android
Now locate the ADK file
C:\Program Files (x86)\Android\android-sdk\tools

sudo npm update -g cordova ionic – did not work

ionic cordova platform update android
C:\Users\Robert\SafariAudio2017>sudo npm update -g cordova ionic
'sudo' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Robert\SafariAudio2017>ionic cordova platform update android
> cordova platform update android
? Running command - failed!

[ERROR] Cordova encountered an error.
        You may get more insight by running the Cordova command above directly.

[ERROR] An error occurred while running cordova platform update android (exit co
de 1):

        Using cordova-fetch for cordova-android@~6.2.2
        Updating android project...
        Error: ENOENT: no such file or directory, open 'C:\Users\Robert\SafariAu
dio2017\platforms\android\AndroidManifest.xml'



C:\Users\Robert\SafariAudio2017>






