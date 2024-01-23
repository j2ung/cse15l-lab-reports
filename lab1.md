# Lab Report 1 - Remote Access and File Systems

## Change Directory Command

   1) `cd` with no arguement

   ```
   {
   [user@sahara ~]$ cd
   [user@sahara ~]$
   }   
   ```

   - The working directory was /home.
   - Since there was no argument to change to a different directory, nothing happened.
   - It is not an error.
     
   2) `cd` with a path to a directory as an argument

   ```
   {
   [user@sahara ~]$ cd lecture1/messages/
   [user@sahara ~/lecture1/messages]$
   }
   ```

   - The working directory was /home.
   - Since the argument was "lecture1/messages/", then the directory was changed to "/home/lecture1/messages/".
   - It is not an error.

   3) `cd` a path to a file as an argument
  
   ```
   {
   [user@sahara ~/lecture1]$ cd Hello.java
   bash: cd: Hello.java: Not a directory
   }
   ```

   - The working directory is /home/lecture1.
   - Since the argument was "Hello.java", it printed an error message.
   - This is an error because the argument requires a directory not a file.
   
   
## List Files Command
   
   1) `ls` with no arguement
   
   ```
   {
   [user@sahara ~]$ ls
   lecture1
   }   
   ```
   
   - The working directory is /home.
   - Since there was no argument, it lists the directory in /home.
   - It is not an error.
    
   2) `ls` with a path to a directory as an argument
   
   ```
   {
   [user@sahara ~]$ ls lecture1/messages
   da.txt   en-us.txt   es-mx.txt   zh-ch.txt
   }
   ```
  
   - The working directory is /home.
   - Since the argument was "lecture1/messages" in the /home directory, it lists the text files in messages.
   - It is not an error.
    
   3) `ls` a path to a file as an argument
   
   ```
   {
   [user@sahara ~]$ ls lecture1/Hello.java
   lecture1/Hello.java
   }   
   ```
   
   - The working directory is /home.
   - Since the argument was "lecture1/Hello.java" and there is nothing to list, the output was "lecture1/Hello.java".
   - It is not an error.
   
   
## Concatenate Command
   
   1) `cat` with no arguement
   
   ```
   {
   [user@sahara ~]$ cat

   }
   ```

   - The working directory is /home.
   - Since there was no argument, there is nothing to concatenate.
   - It is not an error.
    
   2) `cat` with a path to a directory as an argument
   
   ```
   {
   [user@sahara ~]$ cat lecture1/messages
   cat: lecture1/messages: Is a directory
   }
   ```

   - The working directory is /home.
   - Since the argument was "lecture1/messages", there was an error message.
   - This is an error because there is nothing to concatenate in a directory
    
   3) `cat` a path to a file as an argument
  
   ```
   {
   [user@sahara ~/lecture1/messages]$ cat es-mx.txt
   ¡Hola Mundo!
   }
   ```

   - The working directory is /home/lecture/messages.
   - Since the argument was "es-mx.txt", it concatenate the text file and outputs "¡Hola Mundo!".
   - It is not an error.

   
