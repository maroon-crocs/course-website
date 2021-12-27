# Lecture 5 Notes

## 1. `z-index` property

### Dealing with overlapping elements

When you use the `position` property like `position: absolute;` elements "stack" one upon another. Example-

```css
.devices-frame {
  position: relative;
}

.devices-frame video {
  position: absolute;
  left: 119px;
  top: 51px;
  width: 394px;
}
```

```html
<div class="devices-frame">
  <img src="apple-devices-frame.png" />
  <video autoplay playsinline muted loop src="watch-everywhere-vid.m4v"></video>
</div>
```

Output-  
![Z Index Before]("./images/z-index-before.gif")

Notice how after positioning, the video appears to be in front of the screen frame. We want the video to be behind the image frame.

We use the `z-index` property to push the video behind the image.  
The z-index property specifies the stack order of an element.  
An element with a higher stack order (z-index) is always in front of an element with a lower stack order.

By default every element has a `z-index` of 0. So if you want to push the video behind the image you'll have to give it a lower `z-index`.

Example-

```css
.devices-frame {
  position: relative;
}

.devices-frame video {
  position: absolute;
  left: 119px;
  top: 51px;
  width: 394px;
  z-index: -1;
}
```

```html
<div class="devices-frame">
  <img src="apple-devices-frame.png" />
  <video autoplay playsinline muted loop src="watch-everywhere-vid.m4v"></video>
</div>
```

Output-  
![Z Index After]("./images/z-index-after.gif")

## 2. Responsive Websites

### It is a set of techniques that you'll use to adjust a website according to the screen space, this way the website will look good on all devices (desktops, tablets, phones, etc.)

#### **Viewport**

The first step is to add the `meta` `viewport` tag to the `<head>` of the website-

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

#### **Images**

Set all images on the website to a 100% width

```css
img {
  width: 100%;
}
```

#### **Media Queries**

You'll use Media Queries to apply specific CSS to the website as per the device.

```css
@media screen and (max-width: 1024px) {
  p {
    font-size: 18px;
  }
}

@media screen and (max-width: 768px) {
  p {
    font-size: 16px;
  }
}

@media screen and (max-width: 425px) {
  p {
    font-size: 14px;
  }
}

@media screen and (max-width: 375px) {
  p {
    font-size: 12px;
  }
}

@media screen and (max-width: 320px) {
  p {
    font-size: 12px;
  }
}
```

_Note:_  
_i. When using `max-width` in the media query, the `max-width` sizes must be in **descending** order_  
_ii. When using `min-width` in the media query, the `min-width` sizes must be in **ascending** order_
