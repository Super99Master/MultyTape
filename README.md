# Multy Tape
Multy Tape is [Portable Tape](https://github.com/Super99Master/Portable_Tape) 2.0  
It has the same function as Portable Tape plus a way to have multiple SaveState at the same time.  
To switch between projects, you need to specify the name of the project as parameter of the .exe  
Example: "Tape.exe -Project=TheGame"  

## How to use Multy Tape

If you are using MultyTape only to make Tape portable then you just need to keep using Tape as you always did. 
If you want to use the SaveState functions then you need to specify the project to open when lunching Tape.exe.  
Example: "Tape.exe -Project=TheGame"  

The intended way to use MultyTape is via Shortcuts. 
By creating and adding "-Project=YourProject" to the shortcut you can easily have different shortcut that loads different SaveStates.  
If you are working on 2+ Projects and you don't want to keep 1 Big SaveState you can create 2 custom Shortcuts and place them in their respective project folder.  
By doing this you can have a cleaner Tape with less entry, while not losing anything.  

## Installation
* Download [Aeriform Tape](https://www.aeriform.io/docs/tape)
* Right Click on the .exe file you downloaded and open it with 7zip, WinRar or any program that can decompress from .exe files.

| Program | Files To extract |
| ------ | ------ |
| WinRar | All the files shown |
| 7-Zip | Open $PLUGINSDIR and then app-64.7z then select all the files |

* Extract all the files in an empty folder.
* Download the [MultyTape.exe](https://github.com/Super99Master/MultyTape/raw/master/MultyTape.exe) and place it in the same folder
* Run it
* From now on Tape is going to be confined in that folder. Feel free to Move it on a Usb or a Sync Folder.

## How to Upgrade Tape while MultyTape is installed

* Download [Aeriform Tape](https://www.aeriform.io/docs/tape)
* Right Click on the .exe file you downloaded and open it with 7zip, WinRar or any program that can decompress from .exe files.

| Program | Files To extract |
| ------ | ------ |
| WinRar | All the files shown |
| 7-Zip | Open "$PLUGINSDIR" and then "app-64.7z" then select all the files |

* Extract all the files but "Tape.exe" and place them in your Tape folder (Yes, Replace the files in the destination folder)
* Extract Tape.exe on the Desktop or in anyfolder then is not your Tape Folder.
* Rename it "Real_Tape.exe" and move it in your Tape folder (Yes, Replace the file in the destination folder)
* Enjoy the new version!

## How It Works

The first time MultyTape.exe is started it renames the real *Tape.exe* in *Real_Tape.exe* and renames itself *Tape.exe*  
With this all your shortcut should keep working even if the Application is different.

MultyTape then check for Tape file in *%appdata%/Tape* and compares them to his saved file (./multy).  
The newer one gets copied to the other location.  
Then it runs *Real_Tape.exe* and it will detect the copied files and load them.  
When *Real_Tape.exe* is closed MultyTape will recheck each file to see if any of them changed and copy the newer one.  
The last thing it does **IF ENABLED** it deletes *%appdata%/Tape*. Deleting the last proof of ever running the software on your pc.  

## Enable AppData CleanUp
* Run MultyTape at least once
* Go to your Tape folder (where you placed MultyTape.exe)
* Then open "multy" (is a folder)
* Open with any editor "Settings.ini"
* Change "DeleteTapeFolder = False" to "DeleteTapeFolder = True"
* Save

## TODO ?
Make the code more readable.  
Tbh idk if i'm gonna do it. Like the code is pretty small and easy to read it's just very unaesthetic.
