cd
---
```
Command: [user@sahara ~]$ cd
Output: [user@sahara ~]$
```
Working directory: /home <br />
Explanation: Using cd without arguments allows the user to return to the root directory, which is /home in the example. Output is not an error.
```
Command: [user@sahara ~]$ cd lecture1
Output: [user@sahara ~/lecture1]$ 
```
Working directory: /home/lecture1
Explanation: Using cd with a directory as an argument allows the user to change the directory, into lecture1 in this example. Output is not an error.
```
Command: [user@sahara ~/lecture1]$ cd Hello.java
Output: bash: cd: Hello.java: Not a directory
```
Working directory: /home/lecture1
Explanation: Using cd with a file as an argument results in an error, because cd is meant to change into a directory, and a file is an invalid argument which is not a directory.

ls
---
```
Command: [user@sahara ~]$ ls
Output: lecture1
```
Working directory: /home
Explanation: ls displays all directories and files in the current directory. Since we are currently in the root directory home, the only item listed is the directory lecture1. Output is not an error.
```
Command: [user@sahara ~]$ ls lecture1
Output: Hello.class  Hello.java  messages  README
```
Working directory: /home
Explanation: Using ls with a directory argument allows the user to see all available directories and files within the argument directory, which was lecture1 in this case. Output is not an error.
```
Command: [user@sahara ~/lecture1]$ ls Hello.java
Output: Hello.java
```
Working directory: /home/lecture1
Explanation: Using ls with a file argument displays the file itself, since there is no content within a file for the user to access, unlike a directory. Output is not an error.

cat
---
```
Command: [user@sahara ~/lecture1]$ cat
Output: 
```
Working directory: /home/lecture1
Explanation: The output is empty because it is waiting for user input. After it receives the expected input, it will output it. Output is not an error.
```
Command: [user@sahara ~/lecture1]$ cat messages
Output: cat: messages: Is a directory
```
Working directory: /home/lecture1
Explanation: Using cat with a directory results in an error because it is meant to output the contents of a file. By using a directory as the argument, there are no contents to output since it simply leads to more directories and files within the argument directory.
```
Command: [user@sahara ~/lecture1/messages]$ cat en-us.txt 
Output: Hello World!
```
Working directory: /home/lecture1/messages
Explanation: Using cat with a file causes the program to output the contents of the file. Output is not an error.
