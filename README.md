# Altsound-converter
Conversion tool for converting file based sounds to Altsound format

### Linux script for matching folder based sound files to existing altsound.csv files. ###
- Copy script contents to file and make executable with 'chmod +x'
- Place the script in a folder with the altsound.csv file and the 5 sound file subfolders.
- The script will prompt for installation of dialog and ffmpeg packages if they are not previously installed. dialog is required for running the program and ffmpeg for .ogg to .wav conversion.
- Select which of the folders you want to parse and the file type being being parsed .ogg or .wav. 
 - Note that most csv and folder files are of .ogg type but can be converted in both cases to support .wav. Ensure that both the csv and folders have the same file types and if not convert one or the other to so they are in common. I have other scripts for doing either conversion.
- To create a full altsound profile parse all 5 file types (music, jingle, sfx, single and voice).
- Sound profile will be saved to /Altsound folder and include a copy of the altsound.csv file used to parse with.
- If you wish to convert the completed Altsound profile in the /Altsound folder, lastly use the "convert" option once all folders are parsed.
- Some csv files have duplicate address sounds listed where there are no associated folder sounds available. The remove duplicate csv option currently removes duplicate entries where unassociated duplicates have no matching sound files.
- For upload purposes the finished Altsound profile can be zipped using the compression option

 
![](https://i.imgur.com/eFc8p0Y.png)

 
![](https://i.imgur.com/jagkEIr.jpg)
