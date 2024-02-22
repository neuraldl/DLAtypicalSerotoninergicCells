# DLAtypicalSerotoninergicCells

To make the “Shared with me” folder accessible, we need to link this folder to the local/personal drive. We can do this by creating a Shortcut, but this is a manual step, and will be different for everyone. To access a shared with you folder or file in Google Colab, you have to:

Go to Shared with me in Google Drive.
Select the folder or file you want to access.
Right-click on it and choose “Add shortcut to drive”, and a pop-up window will appear, “Select MyDrive”, then click on “Add Shortcut”.
Place the shortcut in a location on your drive that you can find back easily; in the setup I use, the location for Shortcuts is “__Shared”, ensuring that the folder with the shortcuts is at the top of the folder list under “MyDrive”, and then a subdirectory for the organisation.
Rename the shortcut to a meaningful name; I use “DataDevelopement” in this example. The file location and name conventions are very personal, and it doesn’t matter for the program where the files are stored or how they are called, but having some structure can save some headaches later.
![image](https://github.com/neuraldl/DLAtypicalSerotoninergicCells/assets/159064716/c877af4b-87fd-4b41-a151-799eb7d15fba)

Figure 2: Creating a shortcut (image by author)
With the local file system organised, and the personal Google Drive configured, we can try to work with this shared folder in a Python notebook and automate the file sharing in the project.
