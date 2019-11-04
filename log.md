# 100 Days Of Code - Log

### Day 55: November 4, 2019
##### (delete me or comment me out)

**Today's Progress**: Added a new feature to a react to do list - now items get crossed out and moved to the bottom of the list when clicked on. This is my second time doing 100DaysOfCode and I decided to try the journaling component. Started in an external file then remembered I could fork the repo from the challenge.

**Thoughts:** Today I have been continuing to work on a to do list app using react js (react-to-do-app).

I had built in all the primary functionality I wanted: adds items as long as input isn't empty, deletes items by clicking - button, looks nice, has a transition effect when closing/opening.

I also wanted to be able to click on the text of an item to cross it out.

I planned to do this by adding the class... 

.crossed-out {
  text-decoration: line-through;
}

And displaying it with...

className={`item ${(item.isCrossedOut)? "crossed-out" : ""}`}

when an item has been clicked on. The first attempt, where I added a crossedOut: false property to each item (an object representing each list item in the state) worked but also disabled my ability to delete items - as the button was nested inside the li element that had the click event to change cross-out.

I haven't been able to figure out how to access the event object on a function/method that also has other parameters which was my first though to address this problem.

Eventually I came up with a solution - wrapping the item text in a <span> and adding the onClick to that element. This kept the two click items separate and allowed them to work indepently.

I'm not sure if that is the idiomatically react way to do things but it works now.

**Link to work:** [To do list App](https://github.com/JohnathonHutt/react-to-do-list)

