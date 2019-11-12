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

### Day 58: November 7, 2019

**Today's Progress:**

Completed a twitter-bot project using node.js the likes, retweets and follows

**Thoughts:** 

I had originally started this project when learning about REST APIs in Angels Yu's bootcamp course on Udemy. At the time I was getting stuck in 'callback hell' when trying to implement multiple features. I was very new to JS and I wasn't understanding why I couldn't get a list of the tweets outside of the callback to manipulate later - I came back to the project yesterday and could see that it was the asynchronous nature of js that was giving me trouble. I had thought it was a good opportunity to learn more about promises and async await but for better or worse I was able to resolve my issues just by using helper functions - this allowed me to include any functionality I wanted while still keeping the code readable.

**Link to work:** https://github.com/JohnathonHutt/twitter-bot

### Day 61: November 11, 2019

**Today's Progress:**

Finished up a react random quote generator for the freeCodeCamp frontend libraries certificate, also got a good headstart on the markdown previewer.

**Thoughts:** 

The random quote generator was a good opportunity for me to actually use the fetch API (instead of just reading about it). I'd made a futurama themed random quote generator before but I had used hand typed data (that I made for a quiz game). For some reason I hadn't really considered that you could make API requests in the frontend - file and project management is definitely something I need to dive deeper into.

Project challenges - getting react running in codepen took a minute. My use of bootstrap - to make the tweet button look more twitter-y - led to to some undesired consequences (due to a built in "clicked" style on the button class I'm assuming), once I removed bootstrap and styled it with plain CSS the problem went away. I also had an issue with the "tweet" button <a> tag not linking to well anything.. I ended up building a version in create-react-app to test it, it worked fine in the browser - I used encodeURI() to help make the href string out of the tweet which was a new JS function for me to work with.
  
The markdown previewer is coming along nicely - I more or less have the core functionality - just need to play around with it to make sure everything loads and passes tests as desired. Also lots more syling and plenty of functionality to add - I thought the example project looked very nice and I would like to be able to make something with similar functionality - i.e. headers w/ click to expand/fullscreen.

**Link to work:** https://codepen.io/johnathonhutt/pen/dyyKEom

