# Lecture 4 Notes

## 1. Fonts

### In-built Fonts

There are many in-built fonts that we can use, below are some of them-

- Arial
- Verdana
- Helvetica
- Tahoma
- Trebuchet MS
- Times New Roman
- Georgia
- Garamond
- Courier New
- Brush Script MT

We use a specific font like this-

```css
h1 {
  font-family: "Times New Roman";
}
```

```html
<h1>Hello, World!</h1>
```

### External Fonts

You can also use external fonts, one such website from where you can preview and search for fonts is
[Google Fonts](https://fonts.google.com/).

After finding a good font you must copy it's `<link>` code and paste it inside your `<head>`. And then use the `font-family` CSS attribute to use the font.  
Example-

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Web Page</title>

    <!-- Google Fonts Code Start -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap"
      rel="stylesheet"
    />
    <!-- Google Fonts Code End -->

    <style>
      h1 {
        font-family: "Dancing Script", cursive;
      }
    </style>
  </head>

  <body>
    <h1>Hello, World</h1>
  </body>
</html>
```

## 2. Positioning Properties

The `position` property specifies the type of positioning method used for an element (relative, absolute, etc.).

After specifying the position, we must use `top`, `right`, `bottom` and `left` properties to position the element.

- `relative`: An element with `position: relative;` is positioned relative to its normal position.  
  Setting the `top`, `right`, `bottom`, and `left` properties of a relatively-positioned element will cause it to be adjusted away from its normal position.  
  Example-

  ```css
  .box {
    width: 200px;
    height: 200px;
    background-color: red;
    position: relative;
    left: 300px;
    top: 100px;
  }
  ```

  ```html
  <div class="box"></div>
  ```

- `absolute`: An element with `position: absolute;` is positioned `relative` to the nearest **position**ed ancestor (parent).  
  However, if an absolute positioned element has no positioned ancestors, it uses the `<body>` as its parent.  
  Example-

  ```css
  .red-box {
    width: 200px;
    height: 200px;
    background-color: red;
    position: relative;
  }

  .green-box {
    width: 100px;
    height: 100px;
    background-color: green;
    position: absolute;
    bottom: 0px;
    right: 0px;
  }
  ```

  ```html
  <div class="red-box">
    <div class="green-box"></div>
  </div>
  ```

## 3. Centering

You know there are 2 types of elements-

- Inline
- Block

### 1. **Horizontal** Centering

- Inline Elements: Inline elements can be horizontally centered using, `text-align: center;`.  
  Even block elements that contain text **inside of them** can be centered using this technique, example-

```css
h1 {
  text-align: center;
}
```

```html
<h1>Hello, World!</h1>
```

- Block Elements: Block elements can be horizontally centered using, the `margin: auto` trick.  
  For this trick to work, you must specify the `width` of the element to be centered, example-

```css
.box {
  width: 200px;
  height: 200px;
  background-color: red;
  margin: 0 auto 0 auto;
}
```

```html
<div class="box"></div>
```

### 2. **Vertical** Centering

To vertically center an element you'll use the `position: absolute;` trick, example-

```css
#blue-box {
  width: 400px;
  height: 400px;
  background-color: blue;
  position: relative;
}

#red-box {
  width: 200px;
  height: 200px;
  background-color: red;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
```

```html
<div id="blue-box">
  <div id="red-box"></div>
</div>
```

## 4. Images

You can load images in two ways-

- Foreground Image
- Background Image

### 1. Foreground Image

You've already loaded an image as a foreground image. A foreground image is in the front as it doesn't have anything in front of it, example-

```html
<img src="cat.png" />
```

### 2. Background Image

A background image is in the **back**, because there is some text or other things in front of it.  
To load an image in the background, and put other things in front of it we do it this way-

```css
#background-img {
  background-image: url("cat.png");
  background-size: cover;
  background-repeat: no-repeat;
  width: 100vw;
  height: 100vh;
}
```

```html
<div id="background-img">
  <h1>Hello, World!</h1>
</div>
```
