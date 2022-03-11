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


## First Test (481.md)

### Test Case
`[link](/url "title")`
* Our group's implementation output: `['/url "title"']`
* Joe's implemenation output: `[]` 
* Both implementations are wrong because according to CommonMark spec, links are allowed to have titles, which is the part in quotes. However, the title is not actually part of the link so the correct output should be `["/url]`.

### Bug
* For our group's implementation, we would have to do some sort of parsing of titles and links, so a possible idea is that we could split by spaces and take the first
* For Joe's implementation, it is checking if there is a space in the link block, and if there is, then don't include the link. However, we still want to include the link if there is a space between the link and the title
```
// ...
String potentialLink = markdown.substring(openParen + 1, closeParen).trim();
if (potentialLink.indexOf(" ") == -1 && potentialLink.indexOf("\n") == -1) {
    toReturn.add(potentialLink);
    currentIndex = closeParen + 1;
} else {
    currentIndex = currentIndex + 1;
}
// ...
```

## Second Test (577.md)

### Test Case
`![foo](train.jpg)`
* Our group's implementation output: `[]`
* Joe's implemenation output: `[train.jpg]` 
* The correct output would be ours because we are not supposed to include images as links

### Bug
* The example implementation doesn't check if the character before `[` is `!`
* If it is, then it shouldn't be a link and it shouldn't be in the output
```
// ...
int nextOpenBracket = markdown.indexOf("[", currentIndex);
// ...
```








