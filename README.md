## Website Performance Optimization portfolio project

My challenge was to optimize this online portfolio for speed. In particular, I needed to optimize the critical rendering path and make this page render as quickly as possible by applying the techniques I've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To view the results of my work please click the following link:

 [https://pmarkette.github.io/frontend-nanodegree-mobile-portfolio/](https://pmarkette.github.io/frontend-nanodegree-mobile-portfolio)

 This will take you to the landing page that was the focus of Part 1. On the landing page clicking Cam's Pizzeria will take you to pizza.html which is the focus of Part 2.


#### Part 1: Optimize the landing page to achieve a score of at least 90 in [Pagespeed Insights](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fpmarkette.github.io%2Ffrontend-nanodegree-mobile-portfolio).

To optimize index.html I took the following measures:

I optimized the pizzeria image by reducing it's size and running it through a compressor.

I created a tiny thumbnail of the pizzeria image.

I eliminated render-blocking CSS by putting it inline.

I eliminated render-blocking javascript by making it asynchronous.

I prevented the unneccessary loading of print.css by marking it with a media query.


#### Part 2: Optimize Frames per Second in [Cam's Pizzeria](https://pmarkette.github.io/frontend-nanodegree-mobile-portfolio/views/pizza.html)

Scroll up and down to observe how smoothly the backgroud pizzas slide back and forth across the screen. Use the slider to switch between small, medium and large foreground pizzas. Observe how snappy the pizzas resize!

To optimize pizza.html I needed to modify views/js/main.js until the frames per second rate was 60 fps or higher. I also needed to reduce the time to resize pizzas to under 5 ms. 

Here are the measures that I took to achieve this:

I enabled strict mode on all functions.

I used the document.getElementById() Web API call instead of the slower document.querySelector().

I used document.getElementsByClassName() Web API call instead of the slower document.querySelectorAll().

There was a for loop that evaluated an array length property as part of the conditonal statement. I made it a local variable to increase the efficiency of the loop.

When possible I moved Web API calls out of loops and put them into local variables.

I reduced the number of pizzas by making it a function of the screen height.

