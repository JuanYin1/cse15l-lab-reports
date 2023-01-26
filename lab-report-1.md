# Lab Report 1


### Part 1 - Meet Group and open the Google doc
We introduced ourselves and write down names, majors, and best places to study in UCSD into the document.  
And the document is also for use to track what we've done and learned during the lab.  
Here is our report: [report](https://docs.google.com/document/d/1O-gmLX9vhuAqxz7A3dy0n5Z62uy38bucGwAoi9DNQo8/edit?usp=sharing)


---
### Part 2 - Check my 15L Account and change the password
I use the [Link](https://sdacs.ucsd.edu/~icc/index.php) to check my account by type my user name and student ID.  
Then follow the steps on [TUTORIAL](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit) to reset my password. 
After successfully changed my password, during the time of system processing, you could go to the part 3 to instell VScode if you didn't download it yet. 


---
### Part 3 - Install VScode
If you did not download Visual Studio Code, go to the [website](https://code.visualstudio.com/) to install it on your computer.  
If you are using windows operating system, download the `Windows x64` version;  
If you are using mac operating system, download the `maxOS` version:
<img width="1280" alt="截屏2023-01-25 16 31 58" src="https://user-images.githubusercontent.com/79886525/214726930-3ed77334-2a4a-47e8-9ff0-a1ae46f211e4.png">

I already download VScode in my device, and if you successfully download it, it should look like this: 
<img width="1020" alt="截屏2023-01-11 18 00 57" src="https://user-images.githubusercontent.com/79886525/211958283-80b4e80f-7956-4c1c-83a7-1701f1baa431.png">


---
### Part 4 - Connecting my device to school system
Since I use macbook, I don't need to download git.  
Steps I've done this part:  
  1. Type `ssh cs15lwi23and@ieng6.ucsd.edu` and clik enter
  2. Type `yes` and clik enter
  3. Then, it will display a long description like this: 
  <img width="565" alt="截屏2023-01-11 13 46 32" src="https://user-images.githubusercontent.com/79886525/211945433-b471d4e6-1012-425b-b42f-c61751dbcbf4.png">
 
 
---
### Part 5 - Running some commands
I tried some commands like 
`cd ~`, 
`cd`, 
`ls -lat`, 
`ls`, 
`ls -a`, 
`pwd`, 
`cp`, 
`cat`,  
`exit`.  
And the result is like:  
<img width="745" alt="截屏2023-01-11 14 04 00" src="https://user-images.githubusercontent.com/79886525/211946222-2cc5486f-fbe7-44bd-87e4-f3e7200df23a.png">.  
To explain these commands:  
`cd ~` dispaly nothing means it successfully bring me to the home directory.  
`cd` nothing changed
`ls` display the files and directory list of my current location.  
`pwd` shows my current locatiin, which is an abslote path.  
`cp` copy the current file or folder(since I did not use cd to add file, cp dosen't work).  
`cat` print the contents on the current file (since the file dose not exist, cat dosen't work).  
`exit` log out the current account.  
`ls -a`: 
> hidden files start with . (dot) symbol and hidden file are not visible in the regular directory. The (ls -a) command will show the whole list of the current directory including the hidden files.  


---
### Part 6 - Create github accound and use it
#### Create files
1. I already have a github account, and I used this account to create a Repository by cliking the right-top `+` button and then `New repository` botton.  
2. Then follow the [instruction](https://ucsd-cse15l-w23.github.io/week/week1/#editing-markdown) to name it as `cse15l-lab-reports`, and clik the `Create repository` botton.
3. Create a file names `index.md` and added some text, and I create another file, with another name but end with`.md` as well.
4. This is what inside my `cse15l-lab-reports` repository currently:  
<img width="1420" alt="截屏2023-01-11 19 10 06" src="https://user-images.githubusercontent.com/79886525/211967232-e3d0632b-78a5-49ca-b56f-16a505191c0d.png">

#### Display md file using links
1. Go to `setting`, and then choose the `Pages` option in the sidebar. 
2. Change `None` to `main` as the source for Github Pages, and click `Save`. 
3. At the top it’ll say `GitHub Pages source saved`. Wait a bit and refresh the page. 
Eventually you’ll see a message that says `Your site is live at <url here>.` (This can take a few minutes!)
Click the link that’s shown there.
3. A new page pops up, and the text I added in the `index.md` shows up.

What I Found:  
  I added `index.html` to the end of the link, the page will not change.  
  While I chenge another name of my md file, like `text.html`, the page was replaced by the content of `text.md` file
I Learned:  
  The link will display index.md file by defult, but we could change the suffix of the link to show other content of md file 

  
---
### Part 6 - Create lab report file
Refer to the markdown style to create a lab report, which is a good way to do a review.  
Refer to these links:  
  + [what is markdown](https://www.markdownguide.org/getting-started/)  
  + [basic markdown](https://commonmark.org/help/)   
  + [fun fect](https://github.com/ucsd-cse15l-w22/ucsd-cse15l-w22.github.io/blob/main/_posts/weeks/2022-01-10-week2.md)  
  

