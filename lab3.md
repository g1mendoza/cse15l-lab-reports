# Welcome to CSE 15L *Lab Report 3*
## Commands: find
this command recursively traverses the given path and list all files in that directory and subdirectories.


### Use *find* to get a single file by its name

***Ex 1:***

Running the command:

Giselles-MacBook-Pro:docsearch gisellemendoza$ ``` find technical -name "*.txt" ```

The output is very long but part of it looks like the following:
....
```
technical/plos/journal.pbio.0020146.txt

technical/plos/pmed.0020114.txt

technical/plos/pmed.0010028.txt

technical/plos/journal.pbio.0020350.txt

technical/plos/journal.pbio.0020190.txt

technical/plos/pmed.0010029.txt

technical/plos/pmed.0020115.txt

technical/plos/journal.pbio.0020147.txt
```
....

***Ex 2:***

Running the command:

Giselles-MacBook-Pro:docsearch gisellemendoza$ ``` find technical/government/Media -name "*.txt" ```

The output is very long but part of it looks as follows:
```
technical/government/Media/Federal_agency.txt

technical/government/Media/water_fees.txt

technical/government/Media/Helping_Out.txt

technical/government/Media/balance_scales_of_justice.txt

technical/government/Media/BusinessWire2.txt

technical/government/Media/Legal-aid_chief.txt

technical/government/Media/Unusual_Woodburn.txt

technical/government/Media/Funding_cuts_force.txt

technical/government/Media/Good_guys_reward.txt

technical/government/Media/Anthem_Payout.txt
``` 
...

#### What it means:
So we can tell that find is a very useful command that allows us to find different files that are under a certain category. In the second example we see that we get all files under the technical government and media path that are txt files. This is more useful where there are not this many files since if we dont know the exact name of the file but we know the directory is found in we could find that file from using this command. 


### Use *find* to get a single file by its approximate name

***Ex 1:***

Running the command:


### Use *find* to get files by type

***Ex 1:***

Running the command:


### Use *find* to get empty files

***Ex 1:***

Running the command:



### Work Cited
- [Website](https://www.redhat.com/sysadmin/linux-find-command) 
- In class Monday Notes [(1)](https://drive.google.com/file/d/1IvJTh1sfpG28CRI9wH666phLByjwTNJz/view)

