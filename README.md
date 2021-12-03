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


Thank you!
<br /> Learn variable naming convention-> source: https://css-tricks.com/what-do-you-name-color-variables/ 
<br /> source: https://www.w3schools.com/cssref/default.asp
<br /> source: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference 
<br /> blog: https://blog.webdevsimplified.com/2020-02/css-custom-properties/
