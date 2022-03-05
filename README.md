# Altsound-converter
Conversion tool for converting file based sounds to Altsound format

### Linux script for matching folder based sound files to existing altsound.csv files. ###
- Copy script contents to file and make executable with ```chmod +x```
- Place the script in a folder with the altsound.csv file and the 5 sound file subfolders.
- The script will prompt for installation of dialog and ffmpeg packages if they are not previously installed. dialog is required for running the program and ffmpeg for .ogg to .wav conversion.
- Select which of the folders you want to parse and the file type being being parsed .ogg or .wav. 
 - Note that most csv and folder files are of .ogg type but can be converted in both cases to support .wav. Ensure that both the csv and folders use the same file types and if not convert one or the other to so they are in common. If you encounter this convert the original altsound.csv from .ogg to .wav with ```sed -i 's/.ogg/.wav/g'``` altsound.csv. Conversly if you need to convert the altsound.csv from .wav to .ogg use ```sed -i 's/.wav/.ogg/g' altsound.csv```


- To create a full altsound profile parse all 5 file types (music, jingle, sfx, single and voice).
- Sound profile will be saved to /Altsound folder and include a copy of the altsound.csv file used to parse with.
- If you wish to convert the completed Altsound profile in the /Altsound folder, use the "convert" option once all folders are parsed. Selecting this option not only converts the sound files but also appropriately edits the altsound.csv to match.
- Some altsound.csv files have duplicate address sounds listed where there are no associated folder sounds available. The clean_csv option currently removes all duplicate "ID" entries to deal with unassociated ID duplicates that have no matching sound files. In some cases this duplication is used to randomly call different sounds for the same ID. This option is still being developed to make the most out of what is made available for sounds while removing entries that simply cannot be matched due to nothing being available in the original sound folders to be matched to.
- For upload purposes the finished Altsound profile can be zipped using the compression option. This allows you to also specify the profile name which will be the folder name and zip file name after the option is finished.

 
![](https://i.imgur.com/eFc8p0Y.png)

 
![](https://i.imgur.com/jagkEIr.jpg)
