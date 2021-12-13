# Lecture 3 Notes

## 1. CSS Selectors

You must use a **selector** to "select" an HTML element and then apply some style (CSS) on it.  
Syntax (Grammar) of selector \-

```html
<style>
  selector {
    color: red;
  }
</style>
```

These are few of the CSS Selectors-

- _Element_ Selector: You use the HTML Element name as the selector.  
  For Example

  ```css
  h1 {
    color: red;
  }

  li {
    font-size: 20px;
  }
  ```

  ```html
  <h1>Hello, World</h1>
  <ul>
    <li>Monday</li>
    <li>Tuesday</li>
    <li>Wednesday</li>
  </ul>
  ```

- _ID_ Selector: You provide the HTML Element with a **unique** ID and use that ID as the selector.  
  You should use this selector only when you want to select a **specific** element.  
  In CSS, ID selectors should start with the pound/hash sign (**#**).  
   For Example

  ```css
  #title {
    color: red;
  }
  ```

  ```html
  <h1 id="title">Hello, World</h1>
  <ul>
    <li>Monday</li>
    <li>Tuesday</li>
    <li>Wednesday</li>
  </ul>
  ```

- _Class_ Selector: You provide HTML Elements with a class and use that class as the selector.  
  You should use this selector when you want to select a **group** of elements.  
  In CSS, Class selectors should start with the dot sign (**.**).  
   For Example

  ```css
  .holiday {
    color: red;
  }
  ```

  ```html
  <h1>Hello, World</h1>
  <ul>
    <li>Monday</li>
    <li>Tuesday</li>
    <li>Wednesday</li>
    <li>Thursday</li>
    <li>Friday</li>
    <li class="holiday">Saturday</li>
    <li class="holiday">Sunday</li>
  </ul>
  ```

- _Relationship_ Selector: You use the **relationships** of HTML Elements as the selector.  
  For Example

  ```css
  div p {
    font-size: 20px;
  }
  ```

  This will select only that `<p></p>` which is inside a `<div></div>`.

  ```css
  div .title {
    font-size: 20px;
  }
  ```

  And, this will select only that `title` class which is inside a `<div></div>`

  ```html
  <h1 class="title">Hello, World</h1>
  <p>I like computer programming</p>
  <div>
    <h1 class="title">Good Weather</h1>
    <p>Today the weather is fine.</p>
  </div>
  ```

- _Other_ Selector: There are other selectors like-

  - Universal Selector: It is a **universal** selector, meaning it will apply to **all** the HTML Elements. It is denoted by the start (**\***) symbol.  
    For Example

    ```css
    * {
      color: red;
    }
    ```

    ```html
    <h1>Hello, World</h1>
    <ul>
      <li>Monday</li>
      <li>Tuesday</li>
      <li>Wednesday</li>
    </ul>
    ```

  - First Child Selector: It selects those elements that are the **first** child of it's parent.
    For Example

    ```css
    li:first-child {
      color: red;
    }
    ```

    ```html
    <h1>Hello, World</h1>
    <ul>
      <li>Monday</li>
      <li>Tuesday</li>
      <li>Wednesday</li>
    </ul>
    ```

  - Nth Child Selector: It selects a child who is the **nth** child of it's parent.
    For Example

    ```css
    li:nth-child(1) {
      color: red;
    }
    ```

    ```html
    <h1>Hello, World</h1>
    <ul>
      <li>Monday</li>
      <li>Tuesday</li>
      <li>Wednesday</li>
    </ul>
    ```

    You can specify `odd` or `even` in the nth-child to select "odd" or "even" child.

## 2. **Cascading** Style Sheets (CSS)

Meaning of Cascade: Pour downwards.  
If same CSS is applied to an element many times, then the bottom (_Pour downwards_) one will be applied.  
Example-

```css
.box {
  width: 200px;
  height: 200px;
  background-color: red;
  background-color: green;
}
```

```html
<div class="box"></div>
```

Since, `background-color` is applied more than once, the bottom one will be used and the `div` will become green.  
Thus, we say that the most bottom style "overrides" the same styles applied before it.

### Specificity Rule

You know that there are multiple methods to select an HTML element in CSS, like - Element, ID, Class, etc.

If different styles are applied on the same element using different selector methods, which one will be applied?

For Example-

```css
h1 {
  color: red;
}

.title {
  color: green;
}

#title {
  color: blue;
}

div h1 {
  color: orange;
}

div .title {
  color: yellow;
}

div #title {
  color: pink;
}
```

```html
<div>
  <h1 class="title" id="title">Hello, World!</h1>
</div>
```

| Selector | Specificity Weightage |
| -------- | --------------------- |
| ID       | 100                   |
| Class    | 10                    |
| Element  | 1                     |

From this table you can see that ID Selector has the highest weightage, then Class Selector and then Element Selector.

| Selector     | Type              | Total Specificity Weightage |
| ------------ | ----------------- | --------------------------- |
| `h1`         | Element           | 1                           |
| `.title`     | Class             | 10                          |
| `#title`     | ID                | 100                         |
| `div h1`     | Element + Element | 1 + 1 = 2                   |
| `div .title` | Element + Class   | 1 + 10 = 11                 |
| `div #title` | Element + ID      | 1 + 100 = 101               |

Since all these selectors are targeting the **same** element, but the **Total Specificity Weightage** of `div #title` is highest, it will win and it's style will be applied.

## 3. Shorthand Notation

We can use shorthand notation to specify values for `margin`, `padding` and others.  
For 4 values properties like margin and padding the values are given in "clockwise" direction, as-
`top right bottom left`.  
Example-

```css
div {
  margin: 10px 10px 10px 10px;
  padding: 0px 20px 0px 20px;
}
```

```html
<div>
  <h1>Hello, World!</h1>
</div>
```

## 5. Colors

Colors in CSS can be specified using **RGB**, **HEX** and others-

- RGB: An RGB color value is specified with the `rgb()` function, which has the following syntax:
  `rgb(red, green, blue)`.  
   Each parameter (red, green, blue) defines the intensity of the color and can be a number between 0 and 255.  
  Example-

  ```css
  h1 {
    background-color: rgb(255, 0, 0);
  }
  ```

  ```html
  <h1>Hello, World!</h1>
  ```

- Hex: A hexadecimal color is specified with: #RRGGBB, where the RR (red), GG (green) and BB (blue) hexadecimal integers specify the components of the color. All values must be between 00 and FF.
  Example-

  ```css
  h1 {
    background-color: #ff0000;
  }
  ```

  ```html
  <h1>Hello, World!</h1>
  ```

## 6. Pushing Elements using Float

The float property specifies whether an element should float to the left, right, or not at all.  
Example-

```css
#tires img:nth-child(1) {
  float: left;
}

#tires img:nth-child(2) {
  float: right;
}
```

```html
<div id="tires">
  <img src="tire.png" />
  <img src="tire.png" />
</div>
```

## 7. Transformations

The transform property applies a 2D or 3D transformation to an element. It allows you to `rotate`, `scale`, `translate` (move), `skew`, etc., to elements.

For Example-

```css
h1:nth-child(1) {
  transform: rotate(45deg);
}

h1:nth-child(2) {
  transform: translate(500px, 100px);
}

h1:nth-child(3) {
  transform: scale(2.5);
}
```

```html
<div>
  <h1>Hello World!</h1>
  <h1>Hello World!</h1>
  <h1>Hello World!</h1>
</div>
```

## 8. Animations

Animation is a method in which figures are manipulated to appear as moving images.  
In CSS animation is created by slowly changing from one set of CSS styles to another.  
`@keyframes` is used to animate HTML elements using CSS.  
Example-

```css
.box {
  width: 100px;
  height: 100px;
  background-color: red;
  animation: move 2s infinite;
}
```

```css
@keyframes move {
  from {
    transform: translate(0px, 0px);
  }
  to {
    transform: translate(100px, 0px);
  }
}
```

Same things can also be specified as-

```css
@keyframes move {
  0% {
    transform: translate(0px, 0px);
  }
  100% {
    transform: translate(100px, 0px);
  }
}
```

```html
<div class="box"></div>
```
