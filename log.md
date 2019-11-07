# 100 Days Of Code - Log

### Day 55: November 4, 2019

**Today's Progress:**

Added a new feature to a react to do list - now items get crossed out and moved to the bottom of the list when clicked on. This is my second time doing 100DaysOfCode and I decided to try the journaling component. Started in an external file then remembered I could fork the repo from the challenge.

**Thoughts:** 

Today I have been continuing to work on a to do list app using react js (react-to-do-app).

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

Eventually I came up with a solution - wrapping the item text in a span tag and adding the onClick to that element. This kept the two click items separate and allowed them to work indepently.

I'm not sure if that is the idiomatically react way to do things but it works now.

**Link to work:** [To do list App](https://github.com/JohnathonHutt/react-to-do-list)

### Day 56: November 5, 2019

**Today's Progress:**

Finished up the React js section on freeCodeCamp. Started with the redux section.

**Thoughts:** 

The freeCodeCamp material was good practive and reinforced some of the concepts I had covered in the react tutorials from the documentation. Also, itroduced me to some new design patterns - namely doing more of the manipulation in the render() method but before the return (e.g. saving JSX to constants). I think this could be a better approach for readability in a lot of cases.

**Link to work:** n/a

### Day 57: November 6, 2019

**Today's Progress:**

Logging for yesterday* Went to my Wednesday meetup. Started to look at an old node.js project

**Thoughts:** 

At the time I began twitter bot project I was pretty new to JS. I had figured out how to write a like and retweet bot, but not both. I wanted to return a list of tweet ids so that I could perform different operations on them outside of the 'callback jungle'. Everything I knew about scope - which was enough said that this should of worked - but it didn't. The reason was that the code ran on my blank variables before the data could arrive from the API call. I haven't had a chance to take a deeper dive into asynchronous js and promises yet - hopefully this is an opportunity for that.

**Link to work:** n/a

