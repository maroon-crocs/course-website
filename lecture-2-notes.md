# Lecture 2 Notes

## 1. Forms

A form accepts "input" from users, the input can be-

- "text"
- "email"
- "password"
- "tel"
- "checkbox"
- "radio"
- "search"
- "submit"
- "button"

And many more...

This is the syntax (grammer) of the form element, you specify the "type" of input using the `type` attribute

```html
<form>
    <input type="text" placeholder="John Doe"></input>
    <input type="email" placeholder="example@email.com"></input>
    <input type="password" placeholder="Password"></input>
    <input type="tel" placeholder="9088765556"></input>
    <input type="radio" name="gender">Male</input>
    <input type="radio" name="gender">Female</input>
    <input type="checkbox">Running</input>
    <input type="checkbox">Swimming</input>
    <input type="checkbox">Dancing</input>
    <input type="submit"></input>
</form>
```

## 2. Structure of an HTML page (Website)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Website</title>
    <style>
      h1 {
        text-align: center;
      }
    </style>
  </head>
  <body>
    <h1>Hello, World!</h1>
  </body>
</html>
```

You write the `<title>` and the `<style>` (CSS) inside the `<head>`.
You write the actual HTML inside the `<body>`.

## 3. The Box Model

You know that **everything** in HTML is a **BOX**. Even circles, ovals and curves are boxes.

Google-
![Google Box Model]("./images/google-box.png")

Instagram-
![Instagram Box Model]("./images/instagram-box.png")

Every element in a web page is placed according to the box model.
This is how the box model looks-  
![Box Model]("./images/box-model.png")

The Box Model has 4 components-

- Content: It can be any HTML element, e.g. `<h1></h1>`, `<img></img>`, `<div></div>`, `<p></p>`, etc.
- Border: This is the border of the Content.
- Margin: The distance between HTML elements, e.g. if you have have 2 `<img></img>` elements then the distance between them is the margin.
- Padding: The distance between the Border and the Content is known as padding.

Since we have 4 directions - TOP, RIGHT, BOTTOM, LEFT, we can specify border, margin and padding using them.
Example-

```css
img {
  border-top: 10px;
  border-right: 10px;
  border-bottom: 10px;
  border-left: 10px;

  margin-top: 10px;
  margin-right: 10px;
  margin-bottom: 10px;
  margin-left: 10px;

  padding-top: 10px;
  padding-right: 10px;
  padding-bottom: 10px;
  padding-left: 10px;
}
```

## 4. Inline and Block Elements

There are two types of HTML elements-

- Block: They occupy the entire line, even though there is enough space for others. - e.g. `h1`-`h6`, `p`, `div`, `ul`, `li`, etc.
- Inline: They occupy only that much space that is required for them, and leave the remaining space in the line for others. - e.g. `img`, `strong`, `em`, `a`, etc.

To convert inline elements to block elements and vice-versa we use the `display` property in CSS.

Example-

```css
img {
  display: block;
}

h1 {
  display: inline;
}
```

Note: For a block element when there is enough space on the line, we can set `margin-left: auto;` & `margin-right: auto;` to tell the computer to divide the margin "equally" on both left & right side, this way the element will get aligned in center.

### Width & Height of Elements

You can control the size (width & height) of elements using the `width` & `height` property in CSS.

Example:

```css
img {
  width: 100px;
  height: 70px;
}
```

### The `<div>` element

This HTML element is used to create **logical divisions** on the web page.  
It acts as a container which "groups" multiple HTML elements together.

It does not have any visual effect on the content or the layout of its children elements until you apply some style using CSS.

Example-

```html
<div>
    <input type="button" value="Google Search"></input>
    <input type="button" value="I'm Feeling Lucky"></input>
</div>
```

```css
div {
  width: 500px;
}
```

## 5. The `id` attribute selector

When you have multiple HTML tags but want to apply some style on only a specific tag you cannot use the HTML tag name.

```html
<style>
  input {
    width: 100px;
  }
</style>

<input type="button" value="Google Search"></input>
<input type="button" value="I'm Feeling Lucky"></input>
```

In this example the style will apply to both the `input` elements.
If you want to select a "specific" element then you have to use the `id` selector.

The CSS ID selector matches an element based on the value of the HTML element’s `id` attribute.  
In order for the element to be selected, its `id` attribute must match **exactly** the value given in the selector.

Example-

```html
<style>
  #search-button {
    width: 100px;
  }
</style>

<input id="search-button" type="button" value="Google Search"></input>
<input type="button" value="I'm Feeling Lucky"></input>
```

Note: The `id` selector begins with a hash `#`
