# Lab Report #4 - Week 8
---

## Snippet #1

```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)

```

- VSCode Preview:

![Image](/images/vscodesnippet1.png)

### Snippet #1 on VSCode
- According to the VSCode example, we expect the method `getLinks` to return a list that contains ```"`google.com", "google.com", "ucsd.edu"```
- I created a test file for the snippet by creating a new markdown file called `snippet1.md` for it and copy and pasting the snippet code into it 
- From there, I proceeded to create a test method for it in `MarkdownParseTest.java` in my group's repository, as well as the repository we reviewed
- Below is the tester code for the snippet:

![Image](/images/testsnippet1.png)

### My Implementation
- The test failed

![Image](/images/snippet1.png)

- A change that would make my group's code work for this example would be to account for backticks in the file
- If two backticks were found, all the code within them should be ignored when looking for brackets and parentheses

### Implementation my group reviewed
- The test failed

![Image](/images/snippet1.png)


## Snippet #2

```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```

- VSCode Preview:
![Image](/images/vscodesnippet2.png)

### Snippet #2 on VSCode
- According to the VSCode example, we expect the method `getLinks` to return a list that contains ```"`a.com", "a.com(())", "example.com"```
- I created a test file for the snippet by creating a new markdown file called `snippet2.md` for it and copy and pasting the snippet code into it 
- From there, I proceeded to create a test method for it in `MarkdownParseTest.java` in my group's repository, as well as the repository we reviewed
- Below is the tester code for the snippet:
![Image](/images/testsnippet2.png)

### My Implementation
- The test failed
![Image](/images/snippet2.png)
- A change that would make my group's code work for this example would be to add a findCloseParen method (Joe did something like this in class)
- We would also need a method that searches the most inside pair of brackets

### Implementation my group reviewed
- The test failed
![Image](/images/snippet2.png)


## Snippet #3

```
[this title text is really long and takes up more than 
one line
and has some line breaks](
    https://www.twitter.com
)
[this title text is really long and takes up more than 
one line](
    https://ucsd-cse15l-w22.github.io/
)
[this link doesn't have a closing parenthesis](github.com
And there's still some more text after that.
[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/
)
And then there's more text
```

- VSCode Preview:
![Image](/images/vscodesnippet3.png)

### Snippet #3 on VSCode
- According to the VSCode example, we expect the method `getLinks` to return a list that contains ```https://ucsd-cse15l-w22.github.io/```
- I created a test file for the snippet by creating a new markdown file called `snippet3.md` for it and copy and pasting the snippet code into it 
- From there, I proceeded to create a test method for it in `MarkdownParseTest.java` in my group's repository, as well as the repository we reviewed
- Below is the tester code for the snippet:

![Image](/images/testsnippet3.png)

### My Implementation
- The test failed

![Image](/images/snippet3.png)

- A change that would make my group's code work for this example would be to revise the code that considers line breaks
- We would also need to add the condition that if there is only one line break between the parentheses and link test, the test should be counted

### Implementation my group reviewed
- The test failed

![Image](/images/snippet3.png)
