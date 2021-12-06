# Lectures 1 Notes

## 1. File Extensions

Every file has two things-

- Name
- Extension (Format)

Every filename follows the format `filename.extension`

Example -

- `VID-2021-12-02.mp4`, where `VID-2021-12-02` is the filename and `mp4` is the extension
- `resume.pdf`, where `resume` is the filename and `pdf` is the extension
- `IMG-843203.jpg`, where `IMG-843203` is the filename and `jpg` is the extension

## 2. Web Technologies

A website is made up of `HTML`, `CSS`, & `JavaScript`

1. HTML - Defines the structure of the page
2. CSS - Defines the styling (look & feel / aesthetics)
3. JS - Defines the behaviour of the website

### HTML Tags

HTML Tags have an ending element and a closing element, it follows this format- `<tag>Content is added in the between</tag>`.

Every HTML tag must be closed with it's closing HTML tag

Following are some HTML tags-

Heading Elements: They are mostly used for heading texts (Title, Subtitle).
They range from `h1` to `h6`

```html
<h1>Hello, World!</h1>
<h2>Hello, World!</h2>
<h3>Hello, World!</h3>
<h4>Hello, World!</h4>
<h5>Hello, World!</h5>
<h6>Hello, World!</h6>
```

Paragraph Element: It is used when a paragraph is required

```html
<p>The quick brown fox jumps over the lazy dog</p>
```

Strong Element: It signifies that a certain part of a text has a strong importance, seriousness or urgency. Similar to "bold".

```html
<p>Tresspassers will be <strong>prosecuted</strong></p>
```

Emphasis Element: This element signals that a certain part of text has stress emphasis. Similar to "italic".

```html
<p>We <em>ran</em> on seeing the ghost</p>
```

Ordered List: A list where the "order" (numbering/rank) matters, the output will have numbers for each item.

```html
<ol>
  <li>Lion</li>
  <li>Tiger</li>
  <li>Cheetah</li>
  <li>Fox</li>
</ol>
```

Unordered List: A list where the "order" (numbering/rank) DOESN'T matter, the output will have bullet points for each item.

```html
<ul>
  <li>Lion</li>
  <li>Tiger</li>
  <li>Cheetah</li>
  <li>Fox</li>
</ul>
```

Image Element: It is used to load an image.

```html
<img src="cat.jpg"></img>
```

Anchor Element: It is used to link (anchor) an HTML page with another HTML page. The Anchor element is the "Hyper" of `Hyper Text Markup Language` (HTML), meaning you can jump from one page to another just by clicking links.

```html
<a href="some-page.html">Click Here</a>
```

### Attributes of HTML Tags

Every HTML tag has various attributes, they are of this format-

```html
<ram age="25" weight="70"></ram>
```

Here `<ram></ram>` is a tag, `age` and `weight` are its attributes with their respective values.

This `<ram></ram>` tag is just an example to explain attributes of HTML Tags, in reality there is no such tag in HTML.

You've used the below HTML Tags with attributes-

```html
<img src="cat.jpg"></img>
```

Here the `<img>` tag has an attribute `src` with the value `cat.jpg`

```html
<a href="some-page.html">Click Here</a>
```

Here the `<a>` tag has an attribute `href` with the value `some-page.html`

### Nesting HTML Tags

You can nest (put one inside another) one HTML Tag within another like this-

```html
<p>
  <strong><em>India</em></strong> is my <em>country</em>
</p>
```

Another example-

```html
<a href="second.html"><img src="cat.jpeg"></img></a>
```

**Remember** to close the tags properly, the inside one is closed first and then you move outside closing the others on the way.
