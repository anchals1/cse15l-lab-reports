# Anchal Saraswat CSE 15L Lab Report 2

## Screenshot 1: 

**Request:** /add-message?s=Hello

<img width="760" alt="Screenshot 2024-04-23 at 11 52 42 PM" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/d5ddb669-755a-4616-b2ab-7e479906bf3b">


**Description:** In this screenshot, the `public String handleRequest(URI url)` method is being used and that is the method in the Handler class. The relevant argument to this method is the url request as a string, as this determines the action that is done by the web server. The values of relevant fields that are changed include the return message, which gets the string that is entered on the url as input. Also the variable "num", which represents a counter of the number of strings added, initializes to 1 when the first message is entered through the url.

## Screenshot 2: 
**Request:** /add-message?s=How are you

<img width="862" alt="Screenshot 2024-04-23 at 11 52 53 PM" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/7421feff-0bc2-4445-9de0-2b624ef20a1b">

**Description:** In this screenshot, the `public String handleRequest(URI url)` method is also being used and that is the method in the Handler class. The relevant argument is the url request as a string, as this determines the action that is done by the web server. The values of relevant fields that are changed are the return message, which adds the newly entered string("How are you") on the url and has an incremeted number count from the message before. The "num" variable, which represents a counter of the number of messages added, increments by 1, when "How are you" is entered.


Here is my code for StringServer:

<img width="768" alt="Screenshot 2024-04-23 at 11 49 08 PM" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/1bdf4bfa-e910-429f-a076-0ed06d14941d">
<img width="863" alt="Screenshot 2024-04-23 at 11 49 16 PM" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/41558208-bfb4-4655-a3a6-62dacf6937be">

## Part 2:

**Path to private SSH key and public SSH key using ls**

<img width="570" alt="key-path-public" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/c7686a7b-dc92-4127-8140-a9b89a7b00ce">

<img width="712" alt="key-path-private" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/e611bf26-fb98-441a-a9e9-ac117ae335e3">

**Logging into ieng6 with no password:**

<img width="627" alt="no-pw" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/f41b133b-1a3a-4136-be6f-9fe9bc5caf92">


## Part 3:
Someting I learned from lab these past few weeks is that the mkdir command allows the users to create directories through the terminal. Another useful command, scp, allows users to securely transfer files between remote server and local server or two remote servers. One of the most useful commands I learned that I find myself using is man. Running man with another unix command as an argument will give documentation and information about what that command can do for a user.
