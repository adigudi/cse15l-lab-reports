# Lab Report #5 - Week 10
---

## Finding the difference
* Using the following command, I saved the output of my group's implementation
`bash script.sh > group-results.txt` 
* I then did the same thing with Joe's implementation
`bash script.sh > joe-results.txt` 
* I moved both files in the same directory and then ran the diff command
`diff group-results.txt joe-results.txt`
* Output:
```
212c212
< [url]
---
> []
230c230
< [baz]
---
> []
270c270
< []
---
> [/bar\* "ti\*tle"]
...
```

## First Test (577.md)
