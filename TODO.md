clean duplicate csv entries then iterate through each folder indexing sound to csv records then renaming and adding files.

if [[ $CHOICE == "clean_csv" ]]
        then
        cd Altsound
        sort -t, -u -k1,1 altsound.csv > newsound.csv
        mv newsound.csv altsound.csv
        rm newsound.csv
        cd ..
       ./$(basename $0) && exit
fi
