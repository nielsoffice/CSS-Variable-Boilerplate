# CSS-Variable-Boilerplate-
CSS Variable Boilerplate 

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

