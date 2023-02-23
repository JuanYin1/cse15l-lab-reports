# Lab-report-4


### Setup Delete any existing forks of the repository you have on your account  
* Command used: `rm -rf lab7`  
  * Keys pressed: `rm -m l<tab>`  
  * Reason: `<tab>` will search the matched repository for me, which is faster.

--- 


### Setup Fork the repository
Press `Fork` in right up side of the souce code page, so we could have a clone of this repository.

---


### The real deal Start the timer!
start timer. 

---

### Step1: Log into ieng6

* Command used: `ssh cs15lwi23and@ieng6.ucsd.edu`  
  * Keys pressed: `shh <up> <enter>`  
  * Reason: after I type `ssh` and then press `<up>` key, this command will show up since this is the only command related to `ssh` in the search history, so I used up arrow to access it.
  
* After entering my password, press `<Enter>` to log in, and the there is the output of the command:
<img width="764" alt="截屏2023-02-22 14 18 42" src="https://user-images.githubusercontent.com/79886525/220859183-0ffe71d2-b3c5-459f-b347-4a1b89bc070a.png">  


---  


### Step2: Clone your fork of the repository from your Github account 

* Command used: `git clone git@github.com:JuanYin1/lab7.git`  
  * Keys pressed: `git clone <up><up><up><up><up><enter>`  
  * Reason: `git clone` was 5 up my search history, so I could use up arrow access it.  

* The output:
<img width="531" alt="截屏2023-02-22 14 19 42" src="https://user-images.githubusercontent.com/79886525/220859979-307c8730-7262-4928-94ca-3df413e05069.png">  


---



### Step3: Run the tests, demonstrating that they fail
* Command used: `cd lab7/`  
  * Keys pressed: `cd l<tab><enter>`  
  * Reason: go to the working derectory lab7 need to use cd command, and after I type `l`, I press `<tab>` key to let computer find the name-matched folder for me, which is faster.  

* Command used: `ls`  
  * Keys pressed: `ls<enter>`   
  * Reason: I need to know the name of the file, so I need to list them out.  

* Command used: `javac -cp .:lib/hamcrest-core-1.3.jar: lib/junit-4.13.2.jar *. java`  
  * Keys pressed: `javac <up><up><up><up><enter>`  
  * Reason: `javac -cp .:lib/hamcrest-core-1.3.jar: lib/junit-4.13.2.jar *. java` command was 4 up in my search history, so I could use up arrow access it.   

* Command used: `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`  
  * Keys pressed: `java <up><up><up><enter>`  
  * Reason: `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples` command was 3 up in my search history, so I could use up arrow access it.    

* The output:
<img width="830" alt="截屏2023-02-22 14 24 06" src="https://user-images.githubusercontent.com/79886525/220863036-887f17e1-372c-4298-8011-24109509852e.png">  

---


### Step4: Edit the code file to fix the failing test  

#### Before fixing
* Command used: `nano ListExample.java`  
  * Keys pressed: `nano L<tab>java`  
  * Reason: I type `L` and press `tab` to let computer search name-matched file for me, and it gave me `ListExampe.`, so I need to add `java` to make to a complete java file.  
 
* The output:  
<img width="1343" alt="截屏2023-02-22 14 24 31" src="https://user-images.githubusercontent.com/79886525/220863890-f935d2c8-4593-4581-bdd3-52f0dd556971.png">  

After enter the nano, I found the error and fixed it.

#### After fixing  
* Command used: `^o`  
  * Keys pressed: `<cntrol>o <Enter>`  
  * Reason: press control and o at the same time to save the change, then press `enter` to save the modified buffer.  

* The output:  
![image](https://user-images.githubusercontent.com/79886525/220866042-37c24940-cd82-4330-834c-a42bac563a0f.png)  

* Command used: `^x`  
  * Keys used: `<control>x`  
  * Reason: to exit nano.  



---


### Step5: Run the tests, demonstrating that they now succeed  
* Command used: `javac -cp .:lib/hamcrest-core-1.3.jar: lib/junit-4.13.2.jar *. java`  
  * Keys pressed: `javac <up><up><up><enter>`  
  * Reason: `javac -cp .:lib/hamcrest-core-1.3.jar: lib/junit-4.13.2.jar *. java` command was 3 up in my search history, so I could use up arrow access it.   
* Command used: `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`  
  * Keys pressed: `java <up><up><enter>`  
  * Reason: `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples` command was 2 up in my search history, so I could use up arrow access it.  

* The output: 
<img width="970" alt="截屏2023-02-23 01 31 31" src="https://user-images.githubusercontent.com/79886525/220869024-2ebce705-2687-491a-b7bc-e42486a22ef9.png">

As we can see, I fixed the error.


--- 



### Step6: Commit and push the resulting change to your Github account  
* Command used: `git add ListExample.java`  
  * Keys pressed: `git add L<tab><delete>java`   
  * Reason: after typing `git add L`, I press `tab` to help me find the match file, but it shows `ListEcample.class`, so I press `delete` key to delete `class`, and added `java` since I the file I made change is `ListExample.java`.   

* Command used: `git commit -m fixError`  
  * Keys pressed: `git commit -m fixError`  
  * Reason: to commit what I've changed  

* Command used: `git push`  
  * Keys pressed: `git push`  
  * Reason: to push what I've changed, so the fixed filr will show in the website.

* The output:
<img width="492" alt="截屏2023-02-22 14 32 38" src="https://user-images.githubusercontent.com/79886525/220870694-36cde8c1-107a-4bb3-a978-f8d60f938789.png">  


