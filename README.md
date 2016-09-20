# html-css-help

### Structure elements

Structure elements are elements that dictate the structure of the document. Their main purpose is to *hold* other elements.

When styling these elements, the first attributes you should consider styling are:

```
.structure-element {
  height: 500px; // If the content of the element determines it's height, don't include this attribute
  width: 80%;
  margin: 0 auto; // Applying auto to the left and right of the element will center it. If is doesn't work, you might need to adjust the 'display' attribute of the element
  padding: 50px; // Add 'box-sizing: border-box;' to the element if you want the width to include the padding
  background-color: #efefef;
}
```

### Word elements

These elements contain words and include h1, h2, h3, a, span, etc.

When styling these elements, the first attributes you should consider styling are:

```
.word-element {
  color: #000000;
  font-size: 14px;
  font-weight: bold;
  line-height: 18px;
  margin: 0;
}
```

**Note:** in practice, you might only need to use 2 or 3 of these attributes as the default styling will be good enough.

### Aligning elements horizontally

This is one of the trickiest parts of first learning HTML/CSS. There are a number of ways to do this. Some ways are better then others, as such, you should attempt them in the following order. If one way does not work, try the next alternative.

##### 1. inline-block

```
.half-width-box {
  width: 50%;
  display: inline-block;
}
```

##### 2. floating

Floating elements will make them fall next to each other horizontally (if there is space). However, they will fall out of the 'flow' of the HTML which may result in the parent element not being able to contain it. Therefore, you may need to alter the properties of the parent element so it may contain the floated elements:

```
.half-width-box {
  width: 50%;
  float: left;
}
.parent-element {
  overflow: auto; // This will allow the parent element to hold floated elements within it
}
```
