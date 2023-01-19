# Lab Report 


### Part 1 - Meet Group members
We introduced ourselves and write down names, majors, and best places to study in UCSD into the document.  
And the document is also for use to track what we've done and learned during the lab.  
Here is our report: [report](https://docs.google.com/document/d/1O-gmLX9vhuAqxz7A3dy0n5Z62uy38bucGwAoi9DNQo8/edit?usp=sharing)


---
### Part 2 - Download GitHub Desktop
I download the [GitHub Desktop](https://sdacs.ucsd.edu/~icc/index.php) for mac, and it looks like: 
<img width="964" alt="截屏2023-01-18 13 20 59" src="https://user-images.githubusercontent.com/79886525/213299903-26f02df7-8aff-405a-b5a8-8ad6da4b5c79.png">


---
### Part 3 - Clone a Repository
There are two ways to clone a repository to our desttop:
#### Using GitHub website: 
* Go to the repository that you want to clone by logging into my GitHub accound, and clik the `<>clone` botten.
* And choose “Open with Github Desktop” 

#### Using GitHub Desktop
* Find the `file` opition on the left top cornor of your computer, and it will three opitions like this:
<img width="575" alt="截屏2023-01-18 13 21 23" src="https://user-images.githubusercontent.com/79886525/213329514-515d87b7-4031-481a-8bf4-bfe0d10e25dc.png">
* Clik `Clone Repository...`, and choose a repository you need clone.
* (If you just add the repository on your github, you may not find them. Clik refresh botton to refresh it, then it will pop up)
<img width="551" alt="截屏2023-01-18 13 28 06" src="https://user-images.githubusercontent.com/79886525/213330301-c59869f4-a497-4a71-b045-fc869547aed0.png">

After you clone the repository, it will display nothing like this:
<img width="960" alt="截屏2023-01-18 16 55 43" src="https://user-images.githubusercontent.com/79886525/213330513-4b04247f-2b8c-47da-994a-203ff75a7755.png">


---
### Part 4 - Read the files
My partner and I read through the code in the `Server.java` and `NumberServer.java` files, and found out that the code in `NumberServer.java` is checking the format of the URL and give responses:
* If path equals to  `/`, just print out the current visit number
* Else if path is `/increment`, just add current number by 1 and print it out
* Else the path do not have the `/` or `/increment`, check if the url contains `/add`.
  * If it contain `/add`, create a String array to store the strings that URL has, and split them by `=`. 
  * Than find the random count numer inside the URL by finding the key word `count`. And add that number to the num variable. Finally print out the message shows that number has been increased.
  * otherwise, return `404 Not Found!`


---
### Part 5 - Running the Server
There are two ways to running the server:
#### Running on Localhost

#### Running on a Remote Computer 


---
### Part 6 - Create new server
For this part, we create a new java file called SearchEngine.java, and make it to store, add, and search strings we need.
