# CSS

![css logo](https://user-images.githubusercontent.com/22002193/69540470-55a77800-0f8f-11ea-9898-0acd26043695.png)

## What's CSS?

CSS (Cascading Style Sheets) allows you to create great-looking web pages.

![What css looks like](https://user-images.githubusercontent.com/22002193/69540398-2c86e780-0f8f-11ea-9b64-812ed09956fc.jpg)

CSS describes how HTML elements are to be displayed on screen, paper, or in other media.

CSS saves a lot of work. It can control the layout of multiple web pages all at once.

## CSS example

Let's take a look at the following [example](https://codepen.io/shiryz/pen/VwwOBGa?editors=1100#0) in codepen.

As you can see you have an `h1` heading that appears in black, let's change it to red.

- In the CSS tab you can see the following code

```css
h1 {
}
```

- Add the following line of code inside the curly braces: `color: red;`.

- You should see the color changing to red :tada:.

### Analysis

The rule opens with a selector . This selects the HTML element that we are going to style. In this case we are styling level one headings (`<h1>`).

We then have a set of curly braces { }. Inside those will be one or more declarations, which take the form of property and value pairs. Each pair specifies a property of the element(s) we are selecting, then a value that we'd like to give the property.

Before the colon, we have the property, and after the colon, the value. CSS properties have different allowable values, depending on which property is being specified. In our example, we have the color property, which can take various color [values](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#Color).

## CSS syntax and selectors

You can't talk about CSS without meeting selectors. A selector is how we target something in our HTML document in order to apply styles to it. If your styles are not applying then it is likely that your selector does not match the thing you think it should match.

Each CSS rule starts with a selector or a list of selectors in order to tell the browser which elements or elements the rules should apply to.

#### CSS Element Selector

The element selector selects the HTML element by name.

```css
p {
  text-align: center;
  color: blue;
}
```

#### CSS Id Selector

The id selector selects the id attribute of an HTML element to select a specific element. An id is always unique within the page so it is chosen to select a single, unique element.

It is written with the hash character (#), followed by the id of the element.

_Example_

HTML code, the id applies to a specific p tag

```html
<p id="para1">Hello Javatpoint.com</p>
```

Adding rules in the css to the `para1` id

```css
#para1 {
  text-align: center;
  color: blue;
}
```

#### CSS Class Selector

The class selector selects HTML elements with a specific class attribute. It is used with a period character . (full stop symbol) followed by the class name.

_Example_

HTML

```html
<h1 class="center">This heading is blue and center-aligned.</h1>
<p class="center">This paragraph is blue and center-aligned.</p>
```

CSS

```css
.center {
  text-align: center;
  color: blue;
}
```

_Notice_ that the `center` class applies to both the `h1` and the `p` tag, unlike the id selector it is not unique.

## CSS RULES!

Let's practice some css rules, in this [link](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/) go over the exercises of the 'Basic CSS'  section. 

If you are finished with the 'Basic CSS' section go to [Applied Visual Design](https://www.freecodecamp.org/learn/responsive-web-design/applied-visual-design/) and solve these too.

## Task 1 -- Animal Card

Build an animal card that looks like the one you see below. You can choose a different animal, but the design itself should match the one in the example. Your HTML and CSS should be divided into two seperate files. To 'connect' your CSS and HTML files, add the following to your `<head>` element (here the CSS file is called styles.css):  

```html
  <link rel="stylesheet" href="styles.css">
  ```



![](https://i.imgur.com/zWfTYD1.png)

## Task 2 -- Flexbox

The Flexible Box Layout Module (Flexbox) is a CSS3 web layout model. It helps you design a flexible responsive layout structure with ease, without using float or positioning. We will learn the basics of Flexbox by playing a game.

* Please complete the [Flexbox Froggy game](https://flexboxfroggy.com/).
* Use this [Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) to better understand all the   properties.

## ADVANCED CSS :fire: Transitions & Animations

 On w3schools.com, read the following sections and complete the exercises at the bottom (labelled **Test Yourself with Exercises!**)

 - [Transitions](https://www.w3schools.com/css/css3_transitions.asp)
- [Animations](https://www.w3schools.com/css/css3_animations.asp)

### Transitions challenge 
Try to solve this [chalenge](https://codepen.io/jorgecardoso/post/1-css-transitions-and-animations#sec-exercise-1), don't check the solution unless you have tried every possible way you can think of.

Solution can be found in this [file]().
  
## What's next? 
**Go through these games, tutorials, and documentation:**

* Play a game to practice CSS [selectors](https://flukeout.github.io/)
* Practice CSS on the go with [SoloLearn](https://www.sololearn.com/Course/CSS/) 
* Learn about [CSS Grid](https://cssgridgarden.com/) by playing another game
* Codecademy CSS [tutorial](https://www.codecademy.com/learn/learn-css)
* Learn to debug [CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Debugging_CSS)
* Learn to [organize your CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Organizing) 

