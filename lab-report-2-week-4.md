# Lab Report #2 - Week 4

## Code Change #1: Reject extra space between ](
![Image](/images/Code-Error-1.png)

* The failure inducing input was [testcase1.md](https://github.com/adigudi/markdown-parse/blob/main/testcase1.md), where there was an extra space betwwen the closed bracket and the open parentheses. The bug preventing the code from working was that the program would keep looking for the for the open parentheses directly after the closed bracket, just to not find it. This would produce a symptom (screenshot below) where the program would keep running until there was an OutOfMemory error.
 
![Image](/images/testcase1-symptom.png)

## Code Change #2: Fix error and another infinite loop
![Image](/images/Code-Error-2.png)

* The failure inducing input was [testcase2.md](https://github.com/adigudi/markdown-parse/blob/main/testcase2.md), where the backslash would count the character after it as a literal character instead of an operation. The bug preventing the code from working was that the google link should not be printed because of the backslash. This would produce a symptom (screenshot below) where the program would create the google link even though it shouldn't have been created.

![Image](/images/testcase2-symptom.png)

## Code Change #3: Don't include images
![Image](/images/Code-Error-3.png)

* The failure inducing input was [testcase3.md](https://github.com/adigudi/markdown-parse/blob/main/testcase3.md), where there is an exclamation mark before the brackets. The bug preventing the code from working was that the program would count the image syntax as a website link, even though the exclamation mark denotes the code as a link to an image. This would produce a symptom (screenshot below) where the program would add the image link to the ArrayList of website links.

![Image](/images/testcase3-symptom.png)

