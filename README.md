# Altsound-converter
Conversion tool for converting file based sounds to Altsound format

### Linux scripts for matching folder based sound files to existing altsound.csv files. ###

### Use of Sorter vs Digger scripts ###

Sorter and digger are used independently depending on the desitred outcome you are looking for. 

Sorter will provide a mirror copy of the source supplied altsound.csv file to be referenced by the newly generated altsound profile. When using sorter it therefore preserves the original references for commonality with the original sound profile it was pulled from. In doing so it isn't able to add in additional random sounds to be referenced that may have been added by sound profile creators. The end result is likely to require less manual editting but lack some additional variety that may be available.

Digger will generate a new altsound profile with new altsound.csv entries for all sound files it is able to associate. It incrementally "digs" through sound folders and indexes each sound file it finds to a newly generated csv entry and associates it to an exclusive sound file name. It will capture all sound files available and reference them. The negative aspect of this is the the newly generated altsound.csv file will not be congruent with the original altsound.csv ROM folder file used to reference.

- Copy script contents to file and make executable with ```chmod +x sorter```
- Place the script in a folder with the altsound.csv file and the 5 sound file subfolders.
- The script will prompt for installation of depnedencies dialog, ffmpeg and pv if they are not previously installed. dialog is required for running the program menu system, ffmpeg for .ogg to .wav conversion and pv for the zip file progress indicator.
- Select which of the folders you want to parse and the file type being being parsed .ogg or .wav. 
 - Note that most csv and folder files are of .ogg type but can be converted in both cases to support .wav. Ensure that both the csv and folders use the same file types and if not convert one or the other to so they are in common. If you encounter this convert the original altsound.csv from .ogg to .wav with ```sed -i 's/.ogg/.wav/g altsound.csv```. Conversly if you need to convert the altsound.csv from .wav to .ogg use ```sed -i 's/.wav/.ogg/g' altsound.csv```


- To create a full altsound profile parse all 5 file types (music, jingle, sfx, single and voice).
- Sound profile will be saved to /Altsound folder and include a copy of the altsound.csv file used to parse with.
- If you wish to convert the completed Altsound profile in the /Altsound folder, use the "convert" option once all folders are parsed. Selecting this option not only converts the sound files but also appropriately edits the altsound.csv to match.
- Some altsound.csv files have duplicate address sounds listed where there are no associated folder sounds available. The clean_csv option currently removes all duplicate "ID" entries to deal with unassociated ID duplicates that have no matching sound files. In some cases this duplication is used to randomly call different sounds for the same ID. This option is still being developed to make the most out of what is made available for sounds while removing entries that simply cannot be matched due to nothing being available in the original sound folders to be matched to.
- For upload purposes the finished Altsound profile can be zipped using the compression option. This allows you to also specify the profile name which will be the folder name and zip file name after the option is finished.

 
![](https://i.imgur.com/eFc8p0Y.png)

 
![](https://i.imgur.com/jagkEIr.jpg)
