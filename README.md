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
  background-color: var(--global-div-background-primary);
  color: var(--global-text-color);
}
```

# Then you can also overwrite it.
```CSS
p {
  --global-text-color : red; /* assigned as color : ?  */
}
```
<br />
# CSS font properties / attributes

```CSS
font-size:medium|xx-small|x-small|small|large|x-large|xx-large|smaller|larger|length|initial|inherit;
```

Thank you!
<br /> Learn variable naming convention-> source: https://css-tricks.com/what-do-you-name-color-variables/ 
<br /> source: https://www.w3schools.com/cssref/default.asp
<br /> source: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference 
