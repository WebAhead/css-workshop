# CSS Intro

In this section of the workshop you will read through some basic CSS concepts and properties, and straight after a short explaination you will be given a task.

The tasks should be done in the following Codepen -> **[CLICK ME](https://codepen.io/Syborn/pen/ZEbdPQo?editors=1100)**.

## Colors

CSS brings 16,777,216 colors to your disposal. They can take the form of a **name**, an **RGB** (red/green/blue) value or a **hex** code.

##### Example

```css=
h1 {
    /* color name */
    color: red;
    
    /* color as hex code */    
    background-color: #0000ff;
    
    /* color as RGB */
    border-color: rgb(124,252,0);
}
```

#### Tasks:

- Change the **color** and the **background-color** of the title and description in the codepen as you see fit.



## Text

You can alter the size and shape of the text on a web page with a range of properties.

1) **font-family** This is the font itself, such as Times New Roman, Arial, or Verdana.
2) **font-size** sets the size of the font
> html elements such as h1 - h6 have default **font-size** already set
3) **font-weight** states whether the text is bold or not

##### Example

```css

.title {
    font-family: Arial;
    /* px is short for pixels */
    font-size: 20px;
    font-weight: bold;
}

```

#### Tasks:
- [Choose a font from the list](https://www.w3schools.com/cssref/css_websafe_fonts.asp) and add it to the title, description and links.
- set the desctipion **font-size** to 20px. 


## Margins and Padding

margin and padding are the two most commonly used properties for spacing-out elements. A margin is the space **outside** something, whereas padding is the space **inside** something.

![image alt](https://66.media.tumblr.com/ab75c239d85c8b240829d92908114107/tumblr_n9k1ifz3fa1st1te9o1_640.gifv)


##### Example

```css=
.container {
    margin: 10px;
    padding: 25px;
}
```

The four sides of an element can also be set individually.

```css=
.container {
    margin-left: 10px;
    margin-right: 8px;
    margin-top: 50px;
    margin-botton: 1px;
}

.box {
    padding-left: 10px;
    padding-right: 8px;
    padding-top: 50px;
    padding-botton: 1px;
}
```


#### Tasks:
- The links feel like they are too close of each other, give them some using **margin**.
- The text of the links are also very close to the border, give them **padding**.


## Grouping and Nesting

Two ways that you can simplify your code — both HTML and CSS — and make it easier to manage.

#### Grouping
in the following code block you see 3 elements with the same css property

```css=
.title {
    /* as the name suggests it aligns the text in the center */
    text-align: center;
}

.sub-title {
    text-align: center;
}

.description {
    text-align: center;
}
```

instead of repeating the same css properties, you could seperate the selectors with commas and apply CSS properties to all of them:

```css=
.title, .sub-title, .description {
    text-align: center;
}

/* Looks much better now! */
```


#### Nesting 
If the CSS is structured well, there shouldn’t be a need to use many class or ID selectors. This is because you can specify properties to selectors **within** other selectors.
<hr>

Let's say i want to style the following html block:

```htmlmixed=
<footer class="footer">
    <span class="copyright-text">© 2020 WebAhead</span>
</footer>
```

then in the CSS I would do

```css=
.footer {
/* some css here */
}

.copyright-text {
/* some css here */
}
```
<hr>

but instead we can do

```css=
.footer {
/* some css here */
}

.footer span {
/* some css here */
}
```

This removes the need for a class selector in the span.

```htmlmixed=
<footer class="footer">
    <span>© 2020 WebAhead</span>
</footer>
```

<hr>

### Why would I need that ?
Well cause you would have less code on the file!
The lesser the amount of code, the better we can read it which means the faster we can understand and develop.

#### Tasks:
- Instead of adding **font-family** to each text element, group them together and add the **font-family** once.
> Note: you can repeat the same selector multiple times in CSS
> ```css
> .blog, .main {
>     background-color: green;
> }
> 
>  .blog {
>    border: solid 2px blue;
>  }
> ```

- Exercise nesting by applying styling to the div with the `post` class and it's h2.



## Units

CSS has several different units for expressing a length or a size.

##### Some widely used units:
- **px**: pixels
- **%**: percent is relative to the parent element,	`width: 90%;`
- **vw**: viewport width (or screen width), `100vw` being the full viewport's width.
- **vh**: viewport height (or screen height), `100vh` being the full viewport's height, anything higher than `100vh` the page would start scrolling.

#### Tasks:
- try using **vw**, **vh**, **%** and **px** on the colored boxes (`blue-box`, `yellow-box`, `red-box`)


## Media queries
@media at-rules, used to target styles at specific media, such as **screen** or **print**. But this can be pushed to an even greater level of sophistication, enabling you to specify **different design choices depending on screen size**. A page can then be optimized and laid out completely differently for **mobile phones**, **tablets**, and varying browser **window sizes**.


#### Example

```css=
/* if the device has atleast 320px of width and 
 * the width is less than 480px then run the CSS inside
*/
@media (min-width: 320px) and (max-width: 480px) {
    /* this specific media query specifically targets smartphones 
     * in portrait mode */
  .title {
      color: blue;
  }
  
}

/* if the device has atleast 768px of width 
 * it will run the CSS inside
 * also it will override the previous media query
 * which means if we run this CSS code on a device with
 * a width of 800px then the title would be red */
@media (min-width: 768px) {
  
   .title {
      color: red;
   }
  
}
```


workshop inspired by [htmldog.com](https://htmldog.com/guides/css/)