# grep command

## 1. Colorizing Grep results using the --color option  
This command is useful when we need to find a specific pattern in a file while the file is long, or we need to count the times the specific pattern appears.  
This command is going to highlight the specific String in the specific file(s) and print it out by using following command:  
```
grep --color "String" [file]
grep --color "String" [file1] [file2] ...
```

#### Outputs:

<img width="837" alt="截屏2023-02-10 17 48 44" src="https://user-images.githubusercontent.com/79886525/218232571-cede29c9-e9a4-471e-833b-cfb87d64ebf3.png"> 

We could also search the String in multiple files, it will print all of the matched parts in the file1.txt and file2.txt seperately:  

<img width="704" alt="截屏2023-02-10 18 12 26" src="https://user-images.githubusercontent.com/79886525/218233692-710fb6a6-5e15-4542-8b57-dbfb6a6d2581.png"> 


### However:   
We could not search multiple Strings at a time.   
#### Output:  
<img width="699" alt="截屏2023-02-10 18 18 31" src="https://user-images.githubusercontent.com/79886525/218233983-50ce5e05-c4a3-4da3-96fd-97446f903267.png">

#### Source:  
[cyberciti.biz](https://www.cyberciti.biz/tips/howto-see-grep-command-output-in-colours.html)  
[thegeekdiary.com](https://www.thegeekdiary.com/how-to-grep-with-color-output/)



---



## 2. Count the lines where strings are matched with -c option  
This command is going to return a number which represent the number of lines where String are matched in file:  
```
grep -c "String" [file]
// or
grep -c String [file]
```
#### Output: 
<img width="455" alt="截屏2023-02-10 18 38 03" src="https://user-images.githubusercontent.com/79886525/218234921-2e5c6967-5154-41e2-ab41-79748b512dde.png">

As `grep --color`, `grep -c` could also search the String in multiple files, and this time I used `*`:  
<img width="402" alt="截屏2023-02-10 18 54 04" src="https://user-images.githubusercontent.com/79886525/218235392-7060344b-f5d6-49f2-b1c0-b79157f2f538.png">

If could not find matched string, it will return `0`:  
<img width="472" alt="截屏2023-02-10 19 21 55" src="https://user-images.githubusercontent.com/79886525/218236499-3153a46f-7420-4124-9f4f-70c7cfc3633a.png">


#### More information: 
By asking `chatGPT`, I learned that the difference bwteen `grep -c "String"` and `grep -c String` is the first command is batter for string that contains spaces or special characters:  
<img width="822" alt="截屏2023-02-10 19 05 17" src="https://user-images.githubusercontent.com/79886525/218235839-3ad92c1a-2c26-4d70-8bc1-7c8c50eaf6f2.png">

#### Source:  
[digitalocean.com](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix)  
[chatGPT](https://openai.com/blog/chatgpt/)



---



## 3. Number the lines that contain the search pattern with -n option
This command is similar with the `grep color`, insteading of highlight the String, it's going to return the line number.  
This command is going to number the lines where the string pattern is matched , use the `-n` option as shown:
```
grep -n "String" [file]
// or
grep -n String [file]
```
#### Output:
<img width="597" alt="截屏2023-02-10 19 15 05" src="https://user-images.githubusercontent.com/79886525/218236251-2d8455aa-9bcf-4345-bab3-fe842859a32c.png">

  If could not find matched string, it will not return anything(same as `grep --color`):  
  
<img width="513" alt="截屏2023-02-10 19 24 06" src="https://user-images.githubusercontent.com/79886525/218236570-07764c9e-38a2-4e37-a06d-866d466cba5f.png">

#### Source:  
[digitalocean.com](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix)  
[chatGPT](https://openai.com/blog/chatgpt/)



---



## 4. Invert the sense of the search pattern with -v option
This command is used to invert the sense of the search, i.e., it prints only lines that don't match the specified pattern:
```
grep -v String [file]
```

#### Output:
It will print all of the lines that dose not match my input String:  
<img width="581" alt="截屏2023-02-10 19 32 07" src="https://user-images.githubusercontent.com/79886525/218236857-f7553261-5db6-486c-9781-444c9cff3b40.png">
<img width="617" alt="截屏2023-02-10 19 34 57" src="https://user-images.githubusercontent.com/79886525/218236915-c9eb2a71-a7df-46d9-bac2-b9d2a74b08c2.png">

And since almost every line contains "a", it only prints a few lines:  
<img width="463" alt="截屏2023-02-10 19 39 05" src="https://user-images.githubusercontent.com/79886525/218237088-36584085-0a7b-4e46-a0ac-a327bc76a096.png">

By asking `chatGPT`, I learned that `grep -v command` is useful in a variety of scenarios where you want to exclude certain lines from your search results based on a specified pattern:  
<img width="853" alt="截屏2023-02-10 19 41 23" src="https://user-images.githubusercontent.com/79886525/218237141-173aa18d-86bc-4a42-b19a-3a624bc1a9d3.png">

#### Source:  
[digitalocean.com](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix)  
[chatGPT](https://openai.com/blog/chatgpt/)



---  



## More commands
There are other commands of `grep`:  
```
Options Description
-h : Display the matched lines, but do not display the filenames.
-i : Ignores, case for matching
-l : Displays list of a filenames only.
-n : Display the matched lines and their line numbers.
-e exp : Specifies expression with this option. Can use multiple times.
-f file : Takes patterns from file, one per line.
-E : Treats pattern as an extended regular expression (ERE)
-w : Match whole word
-o : Print only the matched parts of a matching line,
 with each such part on a separate output line.

-A n : Prints searched line and nlines after the result.
-B n : Prints searched line and n line before the result.
-C n : Prints searched line and n lines after before the result.

...
```
