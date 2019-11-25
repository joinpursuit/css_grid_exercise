# CSS Grid Lab

1. Play [Grid Garden](https://cssgridgarden.com/) all the way through.

2. Fork and clone this repo. Then, observe our `index.html` file. It should be familiar to you from your Flexbox assignment. Modify only the CSS **Do not edit the HTML**

    This time, it's your task to:

    - Group like colors.
    - Stack them in a single long column, 150px in width.
    - The order of colors should be as follows: red, yellow, blue.
    - Your end product should look like this
    ![9 squates in a column](assets/sample.png)
```
index.html
```
```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>CSS Flexbox</title>
    <link rel="stylesheet" href="./index.css">
  </head>
  <body>
    <div class="blue"></div>
    <div class="red"></div>
    <div class="yellow"></div>
    <div class="blue"></div>
    <div class="red"></div>
    <div class="yellow"></div>
    <div class="blue"></div>
    <div class="red"></div>
    <div class="yellow"></div>
  </body>
</html>

```
```
index.css
```
```
 body {
  display: grid;
  grid-template-columns: 1fr;
  grid-auto-rows: 150px;
  grid-gap: 20px;
}
.red{
  width: 150px;
  height: 150px;
  background-color: red;
  grid-column: 1;
  order: 1;
}

.yellow {
  width: 150px;
  height: 150px;
  background-color: yellow;
  grid-column: 1;
  order: 2;
}


.blue {
  width: 150px;
  height: 150px;
  background-color: blue;
  grid-column: 1;
  order: 3;
}


```


## Bonus

1. Create the HTML and CSS to replicate this layout on a page. Name your files `layout1.html` & `layout1.css`
![grid layout to replicate](assets/grid_layout.png)

```
html
```
```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>CSS Flexbox</title>
    <link rel="stylesheet" href="./layout1.css">
  </head>
  <body>
    <div class="single_square"></div>
    <div class="single_square"></div>
    <div class="single_square"></div>
    <div class="single_square"></div>
    <div class="single_square" id="one"></div>
    <div class="single_square" id="two"></div>
    <div class="single_square" id="three"></div>
    <div class="single_square" id="four"></div>
    <div class="single_square" id="five"></div>
  </body>
</html>
```
```
layout.css
```
```
body {
    display: grid;
    grid-template: repeat(4,150px) / repeat(5,150px);
    grid-gap: 20px;
}

div {
    background-color: yellow;
}

.single_square {
    grid-column: 1;    
}
  
#one {
    grid-area: 1/3;
}

#two {
    grid-area: 1/5;
}

#three {
    grid-area: 2/2/3/4;
}

#four {
    grid-area: 3/3/5/5;
}

#five {
    grid-area: 3/5;
}
```

2. Create the HTML and CSS to replicate a painting by [Mondrian](https://en.wikipedia.org/wiki/Piet_Mondrian). Pick a piece you like or use this one as a starting point. Name your files `mondrian.html` & `mondrian.css`

![image of mondrian painting](assets/mondrian.png)
