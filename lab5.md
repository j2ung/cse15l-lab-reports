# Lab 5 - Putting it All Together

## Part 1 - Debugging Scenario
```
Student

Hello, I am having trouble with my code. Here is the error I am getting:
```
![Image](lab5-ss1.png)
```
I am trying to make a filter and merge method. I want it the filter to return a new list containing
the filtered strings while preserving their original order. As for the merge, I want it to take two
sorted lists of strings and merges them into a single list while maintaining sorted order. Here is
my code:
```
![Image](lab5-ss2.png)

```


TA

Hi there! According to the test, the failure occurred because the expected array and the actual array
have different lengths. This error must be from the merge method. To resolve this issue, you may need
to relook at the implementation of the merge method in the ListExamples class to so it can correctly
merges two sorted lists of strings and returns an array of the expected length with the correct
elements in sorted order. Let me know how it turns out!
```


```
Student

Okay, I rechecked my merge method. I realized my error resided in this method. Specifically, line 37.
I changed it ">" to "<" which perfectly fixed the code. Thank you! Here are my results:
```
![Image](lab5-ss3.png)
![Image](lab5-ss4.png)


## Part 2 - Reflection  
  * One of the things I learned during the last half of the quarter, was the basics of `vim`. Before, I knew nothiing of `vim`. Now, I know a few things like `i` to edit, `:wq`to save changes, and `:q!` to quit without changes. I also learned how to commit and push changes onto Git repositiories. It makes collabortive coding more organized and efficient.
