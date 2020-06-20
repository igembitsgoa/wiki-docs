# Structure of a Page
In this section, we'll look at the structure of a sample page and make some changes that can be submitted later.

Visit [the actual Sample 1 page](https://igembitsgoa.github.io/wiki/Sample1) and then take a look at [the source code for it](https://github.com/igembitsgoa/wiki/blob/master/src/pages/Sample1.pug).

You'll notice correspondence between the code and the page, but also notice that all the details about formatting are neatly hidden away. The build system has been configured to generate all the wrapping code, so you only have to edit this text. Links, colors, animations, everything just works.

The structure looks something like this:
```
extends ../templates/contents.pug

block headVars
    - var title = "Sample 1"
    - var contents = ['Problem', 'Project Design', ...]

block article
    ...

append nextButton
    +button("Design")

//- Citations
    1. doi
    2. doi
    ...

prepend citations
    ...
```

So there are six major sections, which are described in more detail below.

> The most important thing to notice is the indentation of various code blocks. Please keep that in mind as you read the guide.

### 1. `extends ../templates/contents.pug`
This line just says that there some more code that makes this work. Can be safely ignored, but don't modify it.

### 2. `block headVars`
This section contains the title of the page and a list for the table of contents. Please preserve the formatting when you edit it, otherwise it will break.

Links are generated automatically, you just have to change the names of these items, but keep in mind the References section. That has to be added manually (since some pages might not have references).

### 3. `block article`
This is the main body of the page, where all the content lives. The structure of this section has been described in the [article section](article.md).

### 4. `append nextButton`
This section is where you can change the name of the button that leads to the next page. Links and animations just work. All you need to do is change the name in `+button("Name")`. Keep in mind the plus sign and the quotes. It won't work without the plus sign.

### 5. `//- Citations`
This section contains a list of DOIs for citations. All you have to do is enter the doi. All the information is extracted automatically and put in the right places with formatting and links and all that.
More on this in the [citations section](citations.md).

### 6. `prepend citations`
This section is absolutely off limits. Do not touch anything here. Actually you can... it will be over written anyway. Just don't change the warnings in CAPS. That will break things.

Next, we look at a very tiny fraction of the pug language, just enough to edit this wiki. Click [here](pug.md) to proceed.