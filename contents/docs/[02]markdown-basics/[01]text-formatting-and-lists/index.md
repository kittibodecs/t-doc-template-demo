---
type: guide
title: 'Text formatting and lists'
description: 'This guide covers the basics of Markdown text formatting and lists.'
category: markdown-basics
order: 1
---

# Text Formatting and Lists

Markdown is a lightweight markup language for formatting plain text. It makes content creation easy and clean. 
Here’s how to use its essential syntax.

---

## Text Formatting

---

### Headings

Use `#` for headings. The number of `#` symbols determines the level:

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
```

Headings create structure, not only style. Nest them logically and keep them concise. 

Don't use more than one H1 per page.

> Toucan turns headings into anchors for linking.

---

### Bold and Italics

Highlight text by making it italic or bold:

```
Bold: **text** or __text__
Italic: *text* or _text_
Bold and Italic: ***text*** or ___text___
```

Be careful mixing with backticks (`) because backticks show inline code — formatting inside backticks will not work. 

---

### Blockquotes

Use `>` to create blockquotes:

```
> This is a blockquote.
```

Use it to highlight notes, tips, warnings, or quoted text. 

Blockquotes can include bold, italics, inline code, lists, or even images.


---

## Lists

### Unordered Lists

Use `-` or `*` to create unordered lists:

```
- Item 1
- Item 2
  - Subitem 2.1
```

---

### Ordered Lists

Use numbers followed by a period to create ordered lists:

```
1. Item 1
2. Item 2
   1. Subitem 2.1
   - Subitem 2.2
```

Indent them with spaces for nested listing.
 
Also, Markdown will autocorrect if you made a mistake in numbering. 

---

### Nesting

You can nest ordered and unordered lists together:

```
1. Ordered item
   - Subitem 1
   2. Ordered subitem
```

---

## Conclusion

These formatting and list options help structure your content effectively. In the next guide, we’ll explore advanced features like links, images, and tables!
