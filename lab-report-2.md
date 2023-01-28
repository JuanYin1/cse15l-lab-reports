# Part 1
In order to write StringServer.java, I first go to the github and download the [folder](https://github.com/ucsd-cse15l-f22/wavelet) which contans Server.java and NumberServer.java, these two files gives me some hits about how to write code for StringServer.java.  
I open the folder in the vscode, and create a file names `StringServer.java`. 
There are two classes in the StringServer file:  
`Handler` and `StringServer`   
Steps to write my code:
* copy the code inside the main method of the NumberServer.java
* rewrite the code inside the Handler class.

**Explain the setup:**   
The code inside the main method of `NumberServer.java` is the setup part, which is going to read the port of our URL, and create a URL for us. So basiclly we do not need to change it.  
And for the `Handler` class part, we must override the `handleRequest` method because Handler class implements `URLHandler`. Also, we could not change the method header of the method. That's why I need to convert ArrayList to String before return.  
This is my code:  
<img width="885" alt="截屏2023-01-25 20 39 44" src="https://user-images.githubusercontent.com/79886525/214759753-f8aae466-f25c-4215-9816-ab26b09a4745.png">  
<sub>you could also find it from my [github](https://github.com/JuanYin1/CSE15L-lab2/blob/master/NumberServer.java)</sub>.   


---


### What I did in my terminal:
```
javac Server.java StringServer.java
java StringServer 6677
```  

---


### What I did in my url: 
```diff
+ Valid input 1  

https://localhost:6655/add-message?s=first input
https://localhost:6655/add-message?s=second input
https://localhost:6655/add-message?s=third input
https://localhost:6655/
```
the output:  
<img width="448" alt="屏幕截图_20230125_200354" src="https://user-images.githubusercontent.com/79886525/214766359-dd1b883e-b4d6-445c-8fc2-49cf30a49e41.png">


<table>
<thead>
<tr><th>Which methods in your code are called?</th><th>relevant arguments</th><th>How do the values change</th></tr>
</thead>
<tbody>
<tr>
<td>handleRequest(URI url) <br> getPath() <br>contains("/add-message")<br>getQuery()<br>split("=")<br>equals("s")<br>add(parameters[1])<br>add("\n")</td>
<td>URI url:
  <br>https://localhost:6655/add-message?s=first input
  <br>https://localhost:6655/add-message?s=second input
  <br>https://localhost:6655/add-message?s=third input
  <br>https://localhost:6655/
  <br>
  <br>parameters[1]:
  <br>"first input"
  <br>"second input"
  <br>"third input"
  <br>"/"
  </td>
<td>After url be passed into the method as a parameter, there is a if-else if-else statement to check if there is any useful info that could be stored into the ArrayList.<br>  The else if statement found the key word:"add-message", and it also found the Query by calling split and equals methods. <br>Therefore, the String after "=" will be stored into the ArraList<br> And after append three strings into the ArrayList, the fourth command goes to the "if" statement, and I convert the ArrayList to Array and finally to String, after that, I replaced some symbols that should not appear when display the output.</td>
</tr>
</tbody>
</table>


---


```diff
- Invalid input 1  

https://localhost:6677/errorinput
https://localhost:6677/add-message?donothaveequalsign
```
The outputs:  
<img width="305" alt="屏幕截图_20230125_204718" src="https://user-images.githubusercontent.com/79886525/214766409-17118057-9067-4045-917d-4b8600a150a7.png">  
<img width="383" alt="屏幕截图_20230125_204842" src="https://user-images.githubusercontent.com/79886525/214766451-282cde84-3409-4dfd-b3b7-9c7702b5e324.png">



<table>
<thead>
<tr><th>Which methods in your code are called?</th><th>relevant arguments</th><th>How do the values change</th></tr>
</thead>
<tbody>
<tr>
<td>handleRequest(URI url)<br>getPath()</td>
<td>URI url:
  <br>https://localhost:6677/errorinput
  <br>https://localhost:6677/add-message?donothaveequalsign
  </td>
<td>The ArrayList will not change since the command is not right.<br> For the first command, it do not have "add-message" in it's path, so it go to the else statement, and dispaly the Not Found message<br> For second command, it has "add-message" in it's path, so it go to the else if statement, but it do not has "s" key word, so it will show an "addError"</td>
</tr>
</tbody>
</table>


--- 

# Part 2

- My code setup:  
<img width="774" alt="截屏2023-01-25 22 20 11" src="https://user-images.githubusercontent.com/79886525/214770499-6665f8a9-0f29-4a93-914c-7073280c2d59.png">   

- failure-inducing input:  
<pre><code>
    assertEquals(s2, ListExamples.filter(s1, sc));
</code></pre>

- inputs that doesn’t induce a failure:  
<pre><code>
    assertEquals(s3, ListExamples.filter(s5, sc));
    assertEquals(s6, ListExamples.filter(s4, sc));
</code></pre>

- Screenshot of symptom:  
<img width="895" alt="截屏2023-01-26 14 01 46" src="https://user-images.githubusercontent.com/79886525/214960636-55757ad6-db3c-4da3-96d5-e7942997af1f.png">

- The bug:  

Before fix it:  
```  
    static List<String> filter(List<String> list, StringChecker sc) {
      List<String> result = new ArrayList<>();
      for(String s: list) {
        if(sc.checkString(s)) {
          result.add(0, s);
        }
      }
      return result;
    }
```   

After fix it:  
```  
    static List<String> filter(List<String> list, StringChecker sc) {
      List<String> result = new ArrayList<>();
      for(String s: list) {
        if(sc.checkString(s)) {
          result.add(s);
        }
      }
      return result;
    }
```  

- Explain:  
I found that the method returns the correct element, but wrong order.  
And inside the `filter` method, it use for loop and add method to add each element which is valid.   
However, it used `add(index, element)`, which means each time it add element, it will **prepend** element to the arraylist.  
To debug, just remove the `index` part, which means change `add(index, element)` to `add(element)`.


---


# Part 3
### What I learned from lab2:  
* I learned how to compile and run two classes using terminal
* I learned url includes Protocal, Domain, Path and Query
* I learned how to download and update github document through `GitHub Desktop`
* I learned run the server on a remote computer by using `git clone` command



### What I learned from lab3:
* I need to create a concrete class for interface class before I pass an object of that class as a parameter into a method.
* Different operating system uses different commands to run JUnit, but both of them need `-cp` command
* I learned how to undersatnd the test result by checking the output
* I learned `@Test` is one of the annotations of JUnit, which tells JUnit that it is a test case
* When we test method, we could create some variables and using reference to avoid repetitive tests
