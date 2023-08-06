# Markdown

Markdown is a text-to-HTML conversion tool for web writers. Markdown allows you to write using an easy-to-read, easy-to-write plain text format, then convert it to structurally valid XHTML (or HTML).

Documentation: [Markdown Docs](https://daringfireball.net/projects/markdown/)
RFC: [RFC 7763](https://www.rfc-editor.org/rfc/rfc7763)
GitHub Documentation: [Writing Markdown on GitHub](https://docs.github.com/en/get-started/writing-on-github)

---
## Cheat-Sheet

### Headings
```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

Here is a heading: `# Heading`, **don't do this:** `#Heading` 

### Emphasis
```markdown
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
```

### Line Breaks
```markdown
First line with two spaces after.  
And the next line.
```

### Lists

#### Ordered Lists
```markdown
1. First item
2. Second item
3. Third item
```

#### Unordered Lists
```markdown
- First item
- Second item
- Third item
```

### Links
```markdown
Link with text: [link-text](https://www.google.com)
```

### Images
```markdown
Image with alt text: ![alt-text](https://media.tenor.com/x8v1oNUOmg4AAAAd/rickroll-roll.gif)

Image without alt text: ![](https://media.tenor.com/x8v1oNUOmg4AAAAd/rickroll-roll.gif)
```

### Code Blocks

#### Inline Code Block
```markdown
Inline `code` has `back-ticks around` it.
```

#### Blocks of Code
<pre>
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
 
```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```
</pre>

### Tables

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily.

```markdown
| Heading 1 | Heading 2 | Heading 3 |
|---|---|---|
| col1 | col2 | col3 |
| col1 | col2 | col3 |
```

### Task list

To create a task list start line with square brackets with an empty space.
Ex: [ <space> ] and add text for task.
To check the task replace the space between the bracket with "x".

```markdown
[x] Write the post
[ ] Update the website
[ ] Contact the user
```

## Reference

Link: [markdown guide](https://www.markdownguide.org/cheat-sheet)
