# Lab Report #2 - Week 4

## Code Change #1: Reject extra space between ](
![Image](/images/Code-Error-1.png)

* The failure inducing input was [testcase1.md](https://github.com/adigudi/markdown-parse/blob/main/testcase1.md), where there was an extra space betwwen the closed bracket and the open parentheses. The bug preventing the code from working was that the program would cause an error if there was an extra space between the closed bracked and the open parentheses. This would produce a symptom (screenshot below) where the program would keep running until there was an OutOfMemory error.
 
![Image](/images/testcase1-symptom.png)

## Code Change #2: Fix error and another infinite loop
![Image](/images/Code-Error-2.png)
* This is a test

## Code Change #3: Don't include images
![Image](/images/Code-Error-3.png)
* This is a test
