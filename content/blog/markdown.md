+++
title = "Markdown"
+++


<https://commonmark.org/>


## Headings

```md
# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading
```

# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading


## Horizontal Rules

```md
___

---

***
```

___

---

***


## Emphasis

```md
**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~
```

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~


## Blockquotes

```md
> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.
```

> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.


## Lists

### Unordered

```md
+ Create a list by starting a line with `+`, `-`, or `*`
+ Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    * Ac tristique libero volutpat at
    + Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
+ Very easy!
```

+ Create a list by starting a line with `+`, `-`, or `*`
+ Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    * Ac tristique libero volutpat at
    + Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
+ Very easy!

### Ordered

```md
1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa


1. You can use sequential numbers...
1. ...or keep all the numbers as `1.`
```

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa


1. You can use sequential numbers...
1. ...or keep all the numbers as `1.`

### Start numbering with offset:

```md
57. foo
1. bar
```

57. foo
1. bar

### Task list:

```md
- [ ] to be done
- [x] done!
```

- [ ] to be done
- [x] done!


## Code

```md
Inline `code`
```

Inline `code`

### Indented code

```md
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
```

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code


### Block code "fences"

````md
```
Sample text here...
```
````

```
Sample text here...
```

### Syntax highlighting

````md
``` js
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```
````

``` js
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```


## Tables

```md
| Option | No.    | Description  |
| ------ | -----: | :----------- |
| data   |     01 | path to data files to supply the data that will be passed into templates. |
| engine |     02 | engine to be used for processing templates. Handlebars is the default. |
| ext    |     03 | extension to be used for dest files. |
```

| Option | No.    | Description  |
| ------ | -----: | :----------- |
| data   |     01 | path to data files to supply the data that will be passed into templates. |
| engine |     02 | engine to be used for processing templates. Handlebars is the default. |
| ext    |     03 | extension to be used for dest files. |


## Links

```md
Auto-link: https://github.com/

Explicit link: <https://github.com/>

[link text](https://github.com/)

[link with title](https://github.com/ "title text!")
```

Auto-link: https://github.com/

Explicit link: <https://github.com/>

[link text](https://github.com/)

[link with title](https://github.com/ "title text!")


## Images

```md
![Minion](https://octodex.github.com/images/minion.png)
```

![Minion](https://octodex.github.com/images/minion.png)
