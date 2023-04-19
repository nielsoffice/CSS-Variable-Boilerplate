# CSS-Variable-Boilerplate-
CSS Variable Boilerplate ready for Webpack and Gulp.

usage: 
```CSS
var(--global-div-background-primary);
```

OR

# You have to declare the assign type for variable 
```CSS
div {
  background-color: var(--background-primary);
  color: var(--global-text-color);
}
```

# Then you can also overwrite it.
```CSS
p {
  --global-text-color : red; /* assigned as color : ?  */
}
```
#custom variable means not yet exist to the root file
```CSS
# assigning variable directly on css file -> var( --background-color: red );
#  --background-color: this variable is not yet existing so you can assign a value on it.

ex.
body {
  background-color: var(--background-color: red );
  color: var(--global-text-color);
}
```
<br />
# CSS font properties / attributes

```CSS
font-size:medium|xx-small|x-small|small|large|x-large|xx-large|smaller|larger|length|initial|inherit;
```
#Get variable assign to JS 
```javaScript

const getValue = getComputedStyle(document.documentElement).getPropertyValue('--global-text-color');

console.log(getValue);

// output: #93e407 or green !

const btnElement = document.querySelector('.btn-class-name')

btnElement.style.setProperty('--background-color', 'green')

```
<br />
# Google media size Landscape and portrait

```CSS
/* Desktop / Largescreen MAX to MIN mobile approach ! */
@media only screen ... and (max-width: 1368px ) {}
@media only screen ... and (max-width: 1280px ) {}
@media only screen ... and (max-width: 1180px ) {}
@media only screen ... and (max-width: 1024px ) {}
@media only screen ... and (max-width: 992px ) {}
@media only screen ... and (max-width: 915px ) {}
@media only screen ... and (max-width: 896px ) {}
@media only screen ... and (max-width: 851px ) {}
@media only screen ... and (max-width: 844px ) {}
@media only screen ... and (max-width: 820px ) {}
@media only screen ... and (max-width: 800px ) {}
@media only screen ... and (max-width: 768px ) {}
@media only screen ... and (max-width: 740px ) {}
@media only screen ... and (max-width: 720px ) {}
@media only screen ... and (max-width: 667px ) {}
@media only screen ... and (max-width: 653px ) {}
@media only screen ... and (max-width: 600px ) {}
@media only screen ... and (max-width: 540px ) {}
@media only screen ... and (max-width: 480px ) {}
@media only screen ... and (max-width: 428px ) {}
@media only screen ... and (max-width: 414px ) {}
@media only screen ... and (max-width: 412px ) {}
@media only screen ... and (max-width: 393px ) {}
@media only screen ... and (max-width: 390px ) {}
@media only screen ... and (max-width: 375px ) {}
@media only screen ... and (max-width: 360px ) {}
@media only screen ... and (max-width: 320px ) {}

/* Usage : */
/* Check which size are object fit from max size to min size ex. */
@media only screen and (min-width: to_size px ) and (max-width: from_size px ) {}

/* Default | fit for all media screen/font-size*/
/* Principle of mobile first | font-size: must be maintain from min to max for instance 
  *USE this approach in case the design is NOT sensitive, simply means the design just need to be responsive 
   no matter how text and paragraph will break!
*/
@media only screen and (min-width: 667px ) and (max-width: 768px ) {} /* 2 col */ 
/* @media only screen and (min-width: 601px ) and (max-width: 667px ) {}  2 col if necessary! */ 
@media only screen and (min-width: 541px ) and (max-width: 600px /*667 instead!*/ ) {} /* 2 col begin here m to d */ 
@media only screen and (min-width: 481px ) and (max-width: 540px ) {} /* 1 col */
@media only screen and (min-width: 320px ) and (max-width: 480px ) {} /* 1 col */

/* NOTE! */
/* 
Then element or container width must be fit on media assigned, as we have all in one media query above that have capable to handle all media screen in order to fit the font size or typho close to the design mockup on break point the container or specific element width will adjust base on designer media view port assigned untill
we reach the matches close from the mockup. 
For instance designer assigned mobile 428px tablet 992px, and 1080px laptop 1200 for large screen.
instaed of 100% width for sub heading description let adjust the width of container close to the design just for that media requirement 
then allow our all in one purpose media screen adjust for the rest of media size; from all in one 320 to 480 +++ the container manually adjust for 428px where the typhography will match on given mockup*
*We cannot change the font-size for consistency but in order to reach the break of typhography we have to adjust the width instead.
*/

/* Given Break points "AS IS" for layout and prototype 
  *USE this approach in case the design is SUPER sensitive, simply means the design completely must be follow including 
   text or paragraph break, heading text break and image or any object located or position NOT just responsive!
*/
/* GBP Tablet Landscape and Desktop Portrait */
@media only screen and (max-width: 1100px ) { ... }
  /* OR */ @media only screen and (max-width: 1280px ) { ... }
  /* OR */ @media only screen and (max-width: 1080px ) { ... }
  /* OR */ @media only screen and (max-width: 1024px ) { ... }
  
/* GBP Tablet Portrait */
@media only screen and (max-width: 992px ) { ... }
  /* OR */ @media only screen and (max-width: 915px ) { ... }
  /* OR */ @media only screen and (max-width: 880px ) { ... }
  /* OR */ @media only screen and (max-width: 851px ) { ... }
  /* OR */ @media only screen and (max-width: 820px ) { ... }
  /* OR */ @media only screen and (max-width: 780px ) { ... }
  
/* GBP Mobile Landscape: */
@media only screen and (max-width: 768px ) { ... } 
  /* OR */ @media only screen and (max-width: 600px ) { ... } 
  /* OR */ @media only screen and (max-width: 667px ) { ... }
  /* OR */ @media only screen and (max-width: 540px ) { ... }

/* GBP Mobile Portrait: */
@media only screen and (max-width: 480px ) { ... } 
  /* OR */ @media only screen and (max-width: 428px ) { ... } 
  /* OR */ @media only screen and (max-width: 414px ) { ... } 
  /* OR */ @media only screen and (max-width: 412px ) { ... } 
@media only screen and (max-width: 375px ) { ... } 
  /* OR */ @media only screen and (max-width: 360px ) { ... }
  /* OR */ @media only screen and (max-width: 320px ) { ... }

/* Break points fixing contents " In Between " */

/* Principle of mobile first | font-size: must be maintain from min to max for instance */
@media only screen and (min-width: 667px ) and (max-width: 768px ) {} /* 2 col */ 
/* @media only screen and (min-width: 601px ) and (max-width: 667px ) {}  2 col if necessary! */ 
@media only screen and (min-width: 541px ) and (max-width: 600px /*667 instead!*/ ) {} /* 2 col begin here m to d */ 
@media only screen and (min-width: 481px ) and (max-width: 540px ) {} /* 1 col */
@media only screen and (min-width: 320px ) and (max-width: 480px ) {} /* 1 col */

OR >> /* Desktop / Largescreen MAX to MIN mobile approach ! */ [ scroll to top! ]
```

```JS
/* Switch Element top to bottom at media Query <= 540 */
 jQuery(() => {

   jQuery(window).on("resize", function(event){

     let doResize = jQuery(this).width();

     let targetToBringBottom = '#div_block-1579-379'; 
     let targetToBringTop    = '#div_block-1590-379'; 	 

	   const wSize = ( doResize < 540 )	? doResize : false;

	   if (window.matchMedia("(max-width: "+wSize+"px)").matches) {
		  
		  jQuery(targetToBringBottom).insertAfter(jQuery(targetToBringTop)); 
		  jQuery(targetToBringBottom).css({ 'margin-top' : "25px" });  
		  
	   } else if ( doResize >= 540 ) 
	   { jQuery(targetToBringTop).insertAfter(jQuery(targetToBringBottom)); }

    });
    
    jQuery(window).on('load', function () {
  	  
      let doResize = window.screen.availWidth; 
		 
      if ( doResize < requireSize ) {
        jQuery(targetToBringBottom).insertAfter(jQuery(targetToBringTop));
        jQuery(targetToBringTop).css({ 'margin-top' : "25px" });   
      }	
		
    });
    
  });
```
<br />
# CSS GRID 

```CSS
data align
from
1|2 
3|4
------------------------------------------------------
to 
1|3
2|4

parentTag {
 
 grid-template-rows: repeat(3, 1fr);
 grid-auto-flow: column; 

}
link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-flow

------------------------------------------------------
Name and Grid Area
{
display: grid;
gap: 5px;
grid-template-areas:
 "name"
 "email"
 "message"
 "button"
}

link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-areas

------------------------------------------------------
Merge and swapt cells
grid-column-start: // which element tag will selected
grid-row-start:
grid-row-end:
----------------------
grid-column-end: span 2 // expand the button from col1 to col 2 like full-width
OR
grid-column-start: 1
grid-column-end: 3 // no span version

link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-column-start
link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-row-start
link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-row-end

link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-column-end
------------------------------------------------------
justify-content: // Column alignment
align-content: // row alignment
link: https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content
link: https://developer.mozilla.org/en-US/docs/Web/CSS/align-content

------------------------------------------------------
Self alignment

align-self: start;
link: https://developer.mozilla.org/en-US/docs/Web/CSS/align-self
justify-self: end;
link: https://developer.mozilla.org/en-US/docs/Web/CSS/justify-self

------------------------------------------------------
Container Row

parentTag {
 
  display: grid;
  grid-template-rows:  auto, 100px auto// depends on your rows from parent Tag
  // means it have a 3 rows the first got auto height
  // The second got 100px;
  // the third one got auto as well.
}
grid: 
link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid
grid-template-rows:
link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-rows
gap:
Link: https://developer.mozilla.org/en-US/docs/Web/CSS/gap

------------------------------------------------------
Container Alignment

 parentTag {
  
  display: grid;
  grid-template-columns: auto auto auto auto 
  /*
    Using repeat() css function 
    grid-template-columns: repeat(3, auto); // repeat auto 3 times 
  */

 }
 
  link: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns

------------------------------------------------------
Content Alignment
 
 parentTag {
   justify-items:
   align-items:
 }

* Justify-items: 
Link:https://developer.mozilla.org/en-US/docs/Web/CSS/justify-items
* align-items:
Link:https://developer.mozilla.org/en-US/docs/Web/CSS/align-items

/*
 Shorthand: [ justify-items & align-items: ]
 place-items: 
 link: https://developer.mozilla.org/en-US/docs/Web/CSS/place-items
*/
------------------------------------------------------
```
<br />
# Animation

```CSS

div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 4s;  /* place here : mymove  */
  /*
    Properties: 
    animation-name
    animation-duration
    animation-delay
    animation-iteration-count
    animation-direction
    animation-timing-function
    animation-fill-mode
    animation
  */
}

@keyframes mymove {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

Reference: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations
Reference: https://www.w3schools.com/cssref/css3_pr_animation-keyframes.php
https://www.w3schools.com/css/css_math_functions.asp
Library: https://animate.style/

```

Thank you!
<br /> Learn variable naming convention-> source: https://css-tricks.com/what-do-you-name-color-variables/ 
<br /> source: https://www.w3schools.com/cssref/default.asp
<br /> source: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference 
<br /> blog: https://blog.webdevsimplified.com/2020-02/css-custom-properties/
