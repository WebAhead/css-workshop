# CSS transitions solution

Exercises 
https://codepen.io/jorgecardoso/post/1-css-transitions-and-animations#sec-exercise-1

1. 
```css
.anim:active .ball-two {
  left: 500px;
  transition: left .5s ease-in;
  transition-delay: .4s;
}
```

2. 
```css
div {
    width: 100px;
    height: 100px;
    background: red;
	transition: width 2s ease-in-out;	

}
```

3. 
```css
div.one {
	
    width: 100px;
    height: 100px;
    background: red;
	transition: width 1s ease-out;
}

div.two {
    width: 100px;
    height: 100px;
    background: blue;
	transition: width 1s ease-out;
	transition-delay: 1s;
	
}
```

4. 
```css
div#main:hover .topleft {
	transition: all 1s ease;
	transform: rotate(90deg);
	transform-origin: left top;
}
div#main:hover .topright {
	transition: all 1s ease;
	transform: rotate(-90deg);
	transform-origin: top right;
}
div#main:hover .bottomleft {
	transition: all 1s ease;
	transform: rotate(90deg);
	transform-origin: left top;
}

div#main:hover .bottomright {
	transition: all 1s ease;
	transform: rotate(-90deg);
	transform-origin: top right
}
```

5. 
```js
var el = document.querySelector(".box");


el.addEventListener("click", clickedBox, false);

let state = 0 

function clickedBox(evt) {
	
	switch(state) {
		   case 0:
		   	el.style.left = '300px'
		   	break;
		   case 1:
		   	el.style.top = '300px'
		   	break;
		   		   case 2:
		   	el.style.left = '0px'
		   	break;
		   case 3:
		   	el.style.top = '0px'
		   	break;
		default:
			state = 0
		   }
	
	state = state < 3 ? state +1 :  0;
	
}
```
