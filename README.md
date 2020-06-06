# My workings

So I need to find out:

1. How to make the slider scroll to the left and grab the value = **slider.scrollLeft**

2. Grab the value of the X position of the mouse = **After addEventListener() = e.pageX**

3. Add event listeners so that when the user click/holds the mouse and drags, the slider element scrolls in the OPPOSITE direction of the mouse, giving that drag effect

## Important values:

- **page.x** = The x position value of the event (in this case, the mouse's x position because you have an event listener for mouse move)

- **slider.scrollLeft** = This is a number representing the number of pixels that an element has been scrolled to the left

- **slider.offsetLeft** = This is a number representing the number of pixels to the left relative to the left of the parent element that an element is (so e.g it will return 10 if an element is 10px to the left of the left side of it's parent element, like another div)

# Findings from watching Wes' solution:

- **StartX** - Need to find the 'anchor' point - So I needed to store the value of x at which the mouse is clicked down

- **walk = x - startX** - Works out how far the mouse deviates from the initial click point (x) - we then assign this to the scrollleft so the slider moves when we drag but then minus walk again as scroll left was defined initally in the down() function.