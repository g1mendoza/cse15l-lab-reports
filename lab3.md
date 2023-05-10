# Welcome to CSE 15L *Lab Report 3*
## Commands: find
this command recursively traverses the given path and list all files in that directory and subdirectories.

### Use *find* to get a single file by its name

***Ex 1:***

Running the command:

Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical -name "*.txt"```

The output is very long but part of it looks like the following:

....

```technical/plos/journal.pbio.0020146.txt

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

Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical/government/Media -name "*.txt"```

The output is very long but part of it looks as follows:

```technical/government/Media/Federal_agency.txt

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

Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical -iname "*law*txt" 2>/dev/null```

The output looks as follows:

```technical/government/Media//Law_Award_from_College.txt

technical/government/Media//Law_Schools.txt

technical/government/Media//Philly_Lawyers.txt

technical/government/Media//AP_LawSchoolDebts.txt

technical/government/Media//Eviction_law.txt

technical/government/Media//Law-school_grads.txt

technical/government/Media//Texas_Lawyer.txt

technical/government/Media//Poverty_Lawyers.txt

technical/government/Media//Library_Lawyers.txt

technical/government/Media//Wilmington_lawyer.txt

technical/government/Media//Lawyer_Web_Survey.txt
```

***Ex 2:***

Running the command:

Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical -iname "*cvm*txt" 2>/dev/null```

The output looks as follows:

```technical/biomed//cvm-2-1-038.txt

technical/biomed//cvm-2-6-278.txt

technical/biomed//cvm-2-4-180.txt

technical/biomed//cvm-2-6-286.txt

technical/biomed//cvm-2-4-187.txt
```

#### What it means:
Using -imane allows us to search for files when we have an idea of what we want find in the dirrectory we are in but we dont know the full name of what we are looking for. In the first example i showed me trying to access those files that include *law* in their name it then provided me with the name of those files which include *law*. This is useful when we might have several files with simliar names and the one we want to access we dont know its full path.

### Use *find* to get files by type

***Ex 1:***

Running the command:

Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical -type f```

The output is very long but part of it looks as follows:

```technical/plos/journal.pbio.0020146.txt

technical/plos/pmed.0020114.txt

technical/plos/pmed.0010028.txt

technical/plos/journal.pbio.0020350.txt

technical/plos/journal.pbio.0020190.txt

technical/plos/pmed.0010029.txt

technical/plos/pmed.0020115.txt

technical/plos/journal.pbio.0020147.txt

technical/plos/pmed.0020075.txt
```

***Ex 2:***

Running the command:

Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical -type d```

The output looks as follows:

```technical

technical/government

technical/government/About_LSC

technical/government/Env_Prot_Agen

technical/government/Alcohol_Problems

technical/government/Gen_Account_Office

technical/government/Post_Rate_Comm

technical/government/Media

technical/plos

technical/biomed

technical/911report
```

#### What it means:

Using -type allows us to look in our directory and find all those documents that are the type we want. As we see in the first examples typing -type f, loaded all documents that are type file. And this could be done for all types suppoerted such as looking into the directories as well. This is usefull when trying to know how many of these specific types there or simply knowing what excactly there is under those types.

### Use *find* to get empty files

***Ex 1:***

Running the command:

Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical -type f -empty```

The output looks as follows:
``` 
```
its blank!! 


***Ex 2:***

Running the command:
 
Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical -type d -empty```

The output looks as follows:
``` 
```
its blank!! 

#### What it means:

Using -empy after indicating a specific type shows if in that type there is elements that are empty and dont have any contents. In the exampels given there was no empty files or directories therefor there was no specific file or directory returned as we see with the blank output. This is useful becuase if you are trying to work on a file that is empty this could be used to get that file and work on that, it can also be used to determine if there is a need to make more files if we wished to work on an empty one. Overall there are many uses for this command line options. 

## More for fun

### Since the last two commands didnt return anything, we can do try running multiple commands at once! 

Running the commands:

Giselles-MacBook-Pro:docsearch gisellemendoza$ ```find technical -iname "*rr*txt" 2>/dev/null -type f```

The output looks as follows:

```technical/government/Media/Terrorist_Attack.txt

technical/government/Media/Barr_sharpening_ax.txt

technical/biomed/rr73.txt

technical/biomed/rr74.txt

technical/biomed/rr171.txt

technical/biomed/rr167.txt

technical/biomed/rr166.txt

technical/biomed/rr172.txt

technical/biomed/rr37.txt

technical/biomed/rr196.txt

technical/biomed/rr191.txt
```
#### What it means:
Here we see that we are able to use several command options together. This is important since we are able to get more specific facts about what we are trying to find making it easier to access those options that closly match we are looking for. This is extremely useful when there are several files that when using a simple find command will not get us anywhere. 

### Work Cited
- [Website](https://www.redhat.com/sysadmin/linux-find-command) 
- In class Monday Notes [(1)](https://drive.google.com/file/d/1IvJTh1sfpG28CRI9wH666phLByjwTNJz/view)

