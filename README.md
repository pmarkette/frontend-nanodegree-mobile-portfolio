[https://pmarkette.github.io/frontend-nanodegree-mobile-portfolio/](https://pmarkette.github.io/frontend-nanodegree-mobile-portfolio)

## Website Performance Optimization portfolio project

My challenge was to optimize this online portfolio for speed. In particular, I needed to optimize the critical rendering path and make this page render as quickly as possible by applying the techniques I've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).


####Part 1: Optimize index.html to achieve a score of at least 90 in [Pagespeed Insights](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fpmarkette.github.io%2Ffrontend-nanodegree-mobile-portfolio).

To optimize index.html I took the following measures:

I optimized the pizzeria image by reducing it's size and running it through a compressor.
I created a tiny thumbnail of the pizzeria image


####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html I needed to modify views/js/main.js until the frames per second rate was 60 fps or higher. I also needed to reduce the time to resize pizzas to under 5 ms. 

Here are the measures that I took to achieve this:

I enabled strict mode on all functions.
I used the document.getElementById() Web API call instead of the slower document.querySelector().
I used document.getElementsByClassName() Web API call instead of the slower document.querySelectorAll().
There was a for loop that evaluated an array lenght propery as part of the conditonal statement. I made it a local variable to increase the efficiency of the loop.
When possible I moved Web API calls out of loops and put them into local variables.
I reduced the number of pizzas by making it a function of the screen height.

