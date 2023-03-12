# Lab-report-5

## Topic - lab6 review
My grading script:
```
CPATH='.:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar'

rm -rf student-submission
if git clone $1 student-submission; then 
echo 'Finished cloning'
fi

if [[ -f student-submission/ListExamples.java ]]
then
echo "Found the student submission file."
cd student-submission
cp ../TestListExamples.java ./

else
echo "Did not found the student-submission folder"
exit 1
fi

javac -cp $CPATH *.java
if [[ $? -eq 0 ]]
then 
echo "Compile the files successfully"

else
echo "Can not compile the file"

fi
 
java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples > grade.txt
if [[ $? -eq 0 ]]
then
echo "Run the TestListExamples.java file successfully."

else 
echo "Can not run the file"

fi


if grep "There was" grade.txt; then
grep "Tests run:" grade.txt

else 
echo "The test also run successfully."

fi 

echo "Then, I will open try to try to compile and run the GradeServer.java file:"
cd ..
java GradeServer 9999
```

---   

#### Explain my code
Store the compile path to a variable `CPATH`;  
Remove the existing directory which names `student-submission`;  
Clone the files from URL, and create a `student-submission` directory in the current working directory, and store files into the `student-submission` directory ;  
Check if there exists `ListExamples.java` file in `student-submission` directory;
Copy the `TestListExamples.java` file from parent directory to current directory;  
Compile and run the `ListExamples.java` file;  
Store the output into the `grade.txt` file;   
Check the `grade.txt` to see if the file has error by `grep` particular strings;  
Print the result in the terminal;  


---   


#### Concepts include

1. variable declaration:   
Always Capitalize all letters of the name of variable;  
And when we need to use the variable, use `$` before the name of variable.

2. `if git clone $1 student-submission; then`  
We could use command as a statement in if condition, then we could not check the exiting code use `if [[ $? -eq 0 ]]` to check if it works.  

3. `rm -rf` command will delete corresponding directory without questioning
4. Check if the directory exists using `-f` inside if condition   
5. `grep` command used to print the line which includes the particular string  
6. it's good to `echo` the result after each command, therefore user could track the process  
7. If the command is not run successfully, it's good to use `exit 1` to exit the code.


---  



#### Demonstrate it working on several files

1. For the first URL `https://github.com/ucsd-cse15l-f22/list-methods-lab3`:  
Expect: A `failure` message.  
Actual: the output gives a `failure` message:  
<img width="857" alt="截屏2023-03-08 18 34 33" src="https://user-images.githubusercontent.com/79886525/223901180-0c3ce71a-eb93-4dfe-8e54-f23a89f60462.png">  


2. For the second URL `https://github.com/ucsd-cse15l-f22/list-methods-corrected`:  
Expect: A `successful` message.  
Actual: the output gives a `successful` message:  
<img width="894" alt="截屏2023-03-08 18 36 44" src="https://user-images.githubusercontent.com/79886525/223901583-ad0953a9-6483-4753-bfce-f5fca2f589ed.png">  


3. For the third URL `https://github.com/ucsd-cse15l-f22/list-methods-compile-error`:  
Expect: A message that shows `can not compile`.   
Actual: the output gives a `can not compile` message:  
<img width="927" alt="截屏2023-03-08 18 39 17" src="https://user-images.githubusercontent.com/79886525/223902250-2cb1310c-5eaf-4d74-8a8d-3321a3f8a1da.png">  


4. For the fourth URL `https://github.com/ucsd-cse15l-f22/list-methods-signature`:  
Expect: A `successful` message.  
Actual: the output gives a `successful` message:  
<img width="898" alt="截屏2023-03-08 18 44 36" src="https://user-images.githubusercontent.com/79886525/223902686-ac5f0b0c-b014-4d6c-bbd8-762cc5b3abe8.png">  


5. For the fifth URL `https://github.com/ucsd-cse15l-f22/list-methods-filename`:  
Expect: A `Did not found the student-submission folder` message. (since the target file have wrong file name)  
Actual: the output gives a `Did not found the student-submission folder` message:  
<img width="898" alt="截屏2023-03-08 18 46 51" src="https://user-images.githubusercontent.com/79886525/223903057-b7afc162-04f5-453f-ba9a-c1dc7dbbc9d9.png">  


6. For the sixth URL `https://github.com/ucsd-cse15l-f22/list-methods-nested`:  
Expect: A `Did not found the student-submission folder` message. (since the target file in the wrong directory)  
Actual: the output gives a `Did not found the student-submission folder` message:  
<img width="860" alt="截屏2023-03-08 18 52 14" src="https://user-images.githubusercontent.com/79886525/223903886-4dd5ee27-64f9-4456-baaf-a479989c54c0.png">  

7. For the seventh URL `https://github.com/ucsd-cse15l-f22/list-examples-subtle`:  
Expect: A `Can not compile` or `Can not run file`message. (since there is error in files)  
Actual: the output gives a `Can not run the file` and `failure` message:   
<img width="880" alt="截屏2023-03-08 18 54 42" src="https://user-images.githubusercontent.com/79886525/223904318-121cc8a2-78e2-44d6-85b8-d32b99909b95.png">  


