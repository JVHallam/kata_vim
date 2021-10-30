# Tags:
* Setup documentation
* Create tags
* Have an exercise for creating tags
* Use tags to jump to parts of your documentation
* Learn how tags work, then apply this shit
* sessions

* Nah fuck all that, play more with cexpr, cadde, copen and the keys that go with that

* I want some vimscript + file editing stuff in here too
* Everything that can be turned into a vimrun exercise, should
* Git issues with vim diff

# Opening up previously closed files

# Would be nice to have
* file browsing exercise:
	* In one tab, you have the list of commands to do
	* In another tab, you have the file browser
	* You move through setup directory and do things to files, like renaming and what not
    * Tabs, Buffers, Windows, all would be nice to put together in the same set of exercises.

# Cexpr:
* copen

# File Browsing
* Acceptance:
    * I can mark the root of a project
    * I can travel to the root quickly
    * I can search for files
    * I can search through files
    * I can move files
    * I can do a multi file search and replace with consent
    * I can do a multi file search and replace without caring

* Create directory
* Creating files
* Delete files
* Delete directory
* Rename files
* Finding files

* Directory
    * How to check current directory in vim

* netrw commands:
    * hit i to see the timestamps on files

    * file marking:
        * mf - mark a file
        * md - Apply diff to marked files
        * mc - copy marked files

    * Directory marking:
        * mb - mark a directory
        * gb - Go to a bookmarked directory
        * qb - see the bookmarked directorys
        * mB - Remove a book mark
        * 1gb - go to book mark one

    * t - open the file in a new tab
    * f1 to get the help screen
    * Ntree "directory" - Will CD you into a directory

# File browsing and vimscript kata:
## Create the file
* Open the project at it's root
    * cd project_root
    * vim .

* Create the practise_area/browsing directory
    * d practise_area
    * d browsing

* Create the practise_area/browsing/test.vim file
    * % test.vim
    * Go back to :Ex

* Open the file in a new tab
    * t

## Vimscript hello world, with a twist

* Create an array : [ "Hello", "World" ]

* Dump that to a file called "output.txt"
    * call writefile( rotatedState, a:stateFilePath )

* Read it back in
    * contents = readfile( a:stateTemplatePath )

* Echo it
    * echo contents

* Delete the file
    * call delete( filepath )

# Run that from powershell
* This monster will allow you to run vimscript files from bash. I want it to show me the results in realtime though. That'd be nice.
* Can i make vim silent, and pipe the output at the same time?

* vim --cmd "redir! > output.txt" -S ".\test.vim" --not-a-term -c "q!" | Out-null; cat output.txt; 

* This allows you to run vim as a cli interpretter, dropped straight into ex mode!"
    * vim -i NONE -u NORC -U NONE -V1 -nNesS .\test.vim 

* Add -c on the end to close it immediately
    * vim -i NONE -u NORC -U NONE -V1 -nNesS .\test.vim -c "qa!"

## Clean up
* delete the file

* delete the directory
