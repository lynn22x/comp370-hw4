Task 3:
1. How big is the dataset?
ls -lh clean_dialog.csv

2. What’s the structure of the data? (i.e., what are the field and what are values in them)
head -n 1 clean_dialog.csv
head -n 10 clean_dialog.csv

3. How many episodes does it cover?
csvtool col 1 clean_dialog.csv | tail -n +2 | sort | uniq | wc -l


4. During the exploration phase, find at least one aspect of the dataset that is unexpected – meaning that it seems like it could create issues for later analysis.
The speaker is not one pony, sometimes there are two ponies or narrator.

Task 4
grep -c "Twilight Sparkle" clean_dialog.csv
5120
grep -c "Rarity" clean_dialog.csv
3517
grep -c "Pinkie Pie" clean_dialog.csv
3492
grep -c "Rainbow Dash" clean_dialog.csv
3696
grep -c "Fluttershy" clean_dialog.csv
2838
wc -l clean_dialog.csv
36860
