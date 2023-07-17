Description
Windows Batch script to automate batch processing using mkvtoolnix.

Dependencies
MKVToolNix
Usage
Download MKVToolNix.
Open mkvtoolnix-gui.exe.
Add any of the MKV files to be processed (drag-and-drop works just fine).
Perform your changes within the GUI (disable tracks, rename tracks, set default tracks, etc.).
Go to Menu Bar > Multiplexer > Create option file, and save it as 'options.json' in the same directory where all MKV files to be processed are. You can then close the GUI.
Open said JSON file with your favourite editor and completely delete:
The "--output", line along with the one coming right after it.
The "(", and ")", lines together with the one in between them.
Find the mkvmerge.exe executable within MKVToolNix and get its path (Shift + Right-Click > Copy as path from Windows File Explorer).
Download mkvtoolnix-batch.bat from this repository and put it in the directory where all MKV files and the JSON are.
Edit mkvtoolnix-batch.bat and replace "D:\...\mkvmerge.exe" with your path to mkvmerge.exe from step 6.
Run mkvtoolnix-batch.bat by double-clicking it.
Go grab yourself a cup of coffee and wait for the multiplexing process to complete. Processed MKV files will appear inside the mkvmerge_out directory.
Profit.
License
Code licensed under GNU General Public License v3.0.
