# Anchal Saraswat CSE 15L Lab Report 4

## Step 1: Connect to ieng6

Command: `ssh asaraswat@ieng6.ucsd.edu`

**Keys Pressed:** *`<up> <up> <up> <up> <up> <up> <up> <up> <Enter>` 
`ssh asaraswat@ieng6.ucsd.edu` was used 8 commands ago so I pressed the up arrow 8 times to get to that command and then ran to connect to ieng6

IMAGE

## Step 2: Clone repository with SSH url

Command: `git clone git@github.com:anchalsaraswat/lab7.git` `cd lab7`


**Keys Pressed:** *`Ctrl-C: git clone git@github.com:anchalsaraswat/lab7.git` `Typed on command line: git clone` `Ctrl-V` `<Enter>`*
I first used `Ctrl-C` to copy the ssh clone URL from the lab7 Github repository that I forked and then pasted with `Ctrl-V` after the `git clone` command. I pressed enter to clone the forked repository and then `cd lab7` to change the directory to the lab7 repo

IMAGE

## Step 3: Running JUnit Tests with ListExampleTests

Commands:
1. `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar ListExamples.java ListExamplesTests.java`

**Keys Pressed:** *`<up> <up> <up> <up> <up> <Enter>`* `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was used 5 commands ago so I pressed the up arrow 5 times to get to that command and then ran 

2. `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`
   
**Keys Pressed:** *`<up> <up> <up> <up> <up> <Enter>`* After compiling JUnit Test, the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` was used 5 commands ago, so I pressed the up arrow 5 times to get to that command and then ran it to run ListExamplesTests

IMAGE

## Step 4: Edit the code to fix the failing test

**Open File in vim before editing:** 

**Keys Pressed:** `vim ListExamples.java` `<Enter>`

**Edit ListExamples.java File in vim:**

**Keys Pressed:** from cursor at top, left of the file: `329w`, `e`, `x`, `i`, `"2"`, `<esc>` `:wq`
My cursor was at the top left of the file and I wanted to move the cursor to the line with the bug so I moved the cursor forward 329 words with `329w`, moved to the end of the current word "index" with `e` to land on "1" of `index1`, pressed `x` to delete the "1", pressed `i` to enter insert mode, entered "2" to change the variable to `index2`, pressed `<esc>` to go back to normal mode and then used `:wq` to save and exit the file.

IMAGE

## Step 5: Run the tests to show that they now succeed

Commands: 
1. `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ListExamples.java ListExamplesTests.java`

**Keys Pressed:** `<up> <up> <up>` `<Enter>`
`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was used 3 commands ago so I pressed the up arrow 3 times to get to that command and then ran 


2. `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` 

**Keys Pressed:** `<up> <up> <up>` `<Enter>`
After compiling JUnit Test, the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` was used 5 commands ago so I pressed the up arrow 5 times to get to that command and then ran it to run ListExamplesTests

IMAGE 

## Step 6: Commit and push changes to Github

**Keys Pressed:** `git add ListExamples.java` `<Enter>` `git commit -m"changed var"` `<Enter>` `git push` `<Enter>`
After making the edit to ListExamples.java I need the change to show on the remote repository on Github so I did `git add` to add `ListExamples.java` as a file to be included for the commit message and then created the commit with a message "changed var" through `git commit -m"changed var"`. Then I push the changes to my Github repository with `git push` and the edits I commited will show up on GitHub

IMAGE
