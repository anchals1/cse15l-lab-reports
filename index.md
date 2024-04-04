# Anchal Saraswat CSE 15L Lab Report 1
## CD command
1. When no argument is passed the output is:
  <img width="225" alt="cd_noarg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/96f1f097-8ccc-4b55-b691-b7d1ac7acdd8">
  
   The working directory when this command was run is `/home`. I got this output because the `cd` command with no arguments sets the         workng directory to home which is already a given. This is not an error.
   
2. When an argument to a directory is passed the output is:
   
<img width="277" alt="cd_direcarg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/110224cc-2b4a-45a0-98b1-cbf7f030fbe5">
   
  The working directory when `cd lecture1` was passed is `/home/lecture1`. I got this output because `lecture1` is inside the home          directory so when this runs we are changing from `home` to `lecture1`. This is not an error.
   
3. When an argument to a file is passed the output is:
  <img width="375" alt="cd_filearg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/f48763e4-bc69-476f-978e-b8bf4558c463">

  The working directory for `cd messages` is `/home/lecture1/messages` in this case as we are passing an argument to change the             directory to a file in `lecture1` so the `cd` command directs to messages inside `lecture1`. This is not an error.
     
---------------------------------------
## LS command

1. When no argument is passed the output is:
   <img width="204" alt="ls_noarg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/dfa7ee57-3b0b-46f0-9330-711d9e31f3bb">
   
   The working directory when `ls` was run is `/home`. I got this output because the `ls` command with no arguments sets the workng          directory to `home` which is already a given and shows the files in this working directory. This is not an error.
   
2. When an argument to a directory is passed the output is:
   <img width="391" alt="ls_direcarg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/daf4ed69-d098-41ee-9fff-b01075262ed3">
   
   The working directory when `ls lecture1` was passed is also `/home`. I got this output because the `ls` command does not change the       working directory, it lists what is inside the argument. This is not an error.
   
3. When an argument to a file is passed the output is:
  <img width="387" alt="ls_filearg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/9bb9f92b-961e-45ba-b5d3-df9cb5336f71">
  
   The working directory is `/home/lecture1` . I got this output because the `ls Hello.java` command lists the files that are inside the     directory or file we pass as an argument. In this case we are asking it to list the file which is `Hello.java`, so as its output it       returns the name of the file which is a .java file. It does not list the contents. This is not an error
---------------------------------------

## CAT command
1. When no argument is passed the output is:
  <img width="198" alt="cat_noarg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/f60d706d-a9a0-4bf9-b662-ccfd4e32f80c">
  
   The working directory when `cat` was run is `/home`. I got this output because the `cat` command with no arguments does not have          data to read from the input which is missing in this case. This is not an error.
   
2. When an argument to a directory is passed the output is:
  <img width="275" alt="cat_direcarg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/cf23b38c-79b0-4dad-b57a-e7bb145f47fd">
  
   The working directory when `cat lecture1` was passed is also `/home`. I got this output because the `cat` command does not take           directories as arguments, it takes input files that it can read and output. This is not an error.
   
3. When an argument to a file is passed the output is:
  <img width="769" alt="cat_filearg" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/9923ab75-880e-4c21-8e64-04464885c04a">
  
   The working directory when `cat Hello.java` is `/home/lecture1`. I got this output because the `cat` command read the input from the      .java file we gave as an argument and was able to read and output the standard input as well as the import statements and the `git        clone` statement before outputting the standard input. This is not an error.

