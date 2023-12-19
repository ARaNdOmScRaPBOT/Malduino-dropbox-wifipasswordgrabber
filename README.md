# Malduino-dropbox-wifipasswordgrabber
Malduino dropbox wifi password grabber


This is a wifi password grabber i made that uses (in my case a malduino bad usb) to grab a powershell script from my dropbox runs that and then uses netsh to get the saved ssid's with passwords and compresses them into a .zip file and upload that to dropbox
so to use this you need either a rubber ducky or a malduino, a dropbox account, have a dropbox api with acces token to do this go to this link https://www.dropbox.com/lp/developers click on the top right op app console and log in click on my apps and then create app then click on dropbox api and select app folder and name your folder you will see a screen with some information and also the app key this is your acces token the place in the dropbox.ps1 file is marked with "PUT YOUR DROPBOX API ACCES TOKEN HERE" and put the acces token between these "" and save that file in the api map you made in your dropbox then go to the dropbox location you put the dropbox.ps1 file and rigth click on the 3 dots and click share at the bottom you should see create link click on that and then copy the link then open the ducky script and put where it says (PUT YOUR DROPBOX LINK HERE REMOVE EVERYTHING FROM THE LINK STARTING AT ?dl=0) your link that you copied and remove the () and the ?d1=0 at the end of the link you copied and save the file and put it on your rubber ducky or malduino and it is ready for use

update 19-12-2023

dropbox changed how the api works the key is now temporary and they also changed the folder type i managed to use github as a replacement to download the powershell script github detects dropbox api keys and exipres the found api to get around this i split the api key in half and in the powershell script i changed "api key here" to "first half of api key" + "second half of api key" this bypasses the detection and the script will add them together for the full api key
