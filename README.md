## Website Performance Optimization Project

####Project Description
For the Website Performance Optimization project we were asked to (1) optimize `index.html` so that the page gets a score of at least **90** for both mobile and desktop using Google's PageSpeed Insights site and (2) optimize the `main.js` file for the `pizza.html` page so that the page scrolls at **60fps**.

### Part 1: Optimize PageSpeed Insights score for index.html

In order to test the page in [Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) use this project's Github pages URL: https://irishboy922.github.io/fewd-website-optimization-project/

####Optimization Score:
After optimizing the `index.html` page I received a score of **95** for both mobile and desktop.

#####HTML Optimizations
1. Inlined the style.css properties and removed the link tag.
2. Placed a `media="print"` attribute to the `print.css` link tag.
3. Inlined the `perfmatters.js` javascript code into the index.html file.
4. Removed the `perfmatters.js` script tag.
5. Added an `async` attribute to the Google Anylitics script tag.
6. Moved the inline Google Analytics code to the bottom of the page, right before the closing body tag.

#####CSS
1. Minified the `print.css` file and redirected the `print.css` link tag to the minified version.

#####IMAGES
1. Created a thumbnail size version of the `pizzeria.jpg` file and placed it in the `img/` folder.
2. Compressed all the files in the `img/` folder.


### Part 2: Optimize Frames per Second in pizza.html

#### Frame Rate

#####updatePositions() Function Modifications
1. Moved the `var items = document.querySelectorAll('.mover');` outside of the `updatePositions()` function.
2. Changed the `querySelectorAll` to `getElementsByClassName`.
3. Assigned the `items.length` to the variable `itemsLen`.
4. Created an empty var `phase` outside the `for` loop.
5. Called `updatePositions` function in a `requestAnimationFrame()`.

#####Pizza elements Modifications
1. Reduced the number of pizza elements to be created from 200 to 30.
2. Removed the width and height declarations from the `for` loop and gave the `.mover` class in the `views/css/style.css` sheet the width value of `73.333px` and a height value of `100px`.

#### Computational Efficiency
Was able to reduce the time to resize pizza's down to **0.66ms**.
#####changePizzaSizez() Function Modifications
1. Created a variable `pizzaContainers` to store an array of all the `randomPizzaContainer`'s and eliminate redundant code.
2. Removed the `determinDx` function and placed the `sizeSwitcher` function inside the `changePizzaSizes` function.
3. Refactored the `switch` to work inside the `changePizzaSizes` function.
4. Refactored the `changePizzaSizes` code to give the pizza's a percentage value for the new width.
 
