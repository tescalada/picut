picut is a project to create a pure shortcut keyboard with a pi 0 for use in blender or other heavy shortcut applications.

The pi0 will work as a keyboard gadget, with a bluetooth keyboard attached

on startup a python script will start that is reading the input from the local keyboard, and outputting shortcuts to the host computer

the shortcuts will be stored in json files with the ability to load a custom file using a shortcut, and the ability to write new shortcuts to the file using a key combination

the shortcut json files will be saved in /opt/picut/config/[0-9a-zA-Z].json

to enter command mode press ctrl-shift-c

Commands:

    load a new config:
        l [0-9a-zA-Z]
            this will load the the config file with the character entered (or create a new one if one does not exist)

    add a shortcut:
        s shortcut_sequence return key return
            this will assign the shortcut_sequence to the key entered

    find a shortcut:
        s shortcut_sequence return return
            this will show on the display the keyboard key associated with the entered shortcut sequence if any exists




whenever a letter is pressed, the shortcut sequence will be looked up for that letter in the json file and sent to the host computer

if equipped with a display, it will display the name of the config file loaded and the shortcut sent for the last key entered.
when in load-config mode it will display the available config files and names
when in 

this project is similar to https://randomnerdtutorials.com/raspberry-pi-zero-usb-keyboard-hid/ so I will be starting from there for setup of the pi and initial python applications
