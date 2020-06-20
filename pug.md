# The Pug Templating Language
If you're familiar with HTML, you'll notice that Pug is similar, but much more simplified. 

Here's a sample block of code:
```
h1 This is a heading.
p This is a paragraph.
p.
    This is a multi-line paragraph. 
    All lines here must be indented. 
    Even if you break lines here, it won't matter.
    They will show as part of the same paragraph.
```

Notice that whatever follows `h1` is a heading. We similarly have `h2`, `h3` and so on. 

For a paragraph, the `p` tag is required. If the paragraph is short and can fit in one line on your screen, 
```
p Writing like this is fine.
```
But if the paragraph spans multiple lines, you'll have to split it manually. Please make sure the text doesn't flow beyond the width of your screen.

For this, the multi-line syntax is used, shown below.
```
p.
    This is a multi line paragraph.
```

If you add a dot after a tag, everything in the next block of code is part of that. So multiple lines will also be read as part of the same paragraph, as long as they are indented properly.

That's all about pug for now. More documentation is available [here](https://pugjs.org/language/attributes.html) for those interested. 

In the next section, we look at the structure of the `article` block, which contains the main body of the page. Click [here](article.md) to continue.

