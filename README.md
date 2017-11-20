# 100DaysOfCode

### Day 69-75: November 14-20, 2017

**Today's Progress**:
1. I'm in holidays, watched ES6 course by Wes Bos and learned how to use animations and transitions with Vue.js.
### Day 68: November 14, 2017    

**Today's Progress**:   
1. Today I finished with CSS Animations by [@TheNetNinjaUK](https://www.youtube.com/channel/UCW5YeuERMmlnqo4oq8vwUpg).  

### Day 67: November 13, 2017    

**Today's Progress**:   
1. Today I started with CSS Animations by [@TheNetNinjaUK](https://www.youtube.com/channel/UCW5YeuERMmlnqo4oq8vwUpg).  

**Thoughts**:     
1. I've learnt about  Animations, transitions and keyrames.
### Day 66: November 11, 2017    

**Today's Progress**:   
1. Today I finished with Udacity's Responsive Web Design Course.  

**Thoughts**:     
1. I've learnt about Responsive Tables and Fonts.  
2. Minor breakpoints.    
### Day 65: November 10, 2017    

**Today's Progress**:   
1. Today I continued with Udacity's Responsive Web Design Course.  

**Thoughts**:     
1. I've learnt about Design Patterns.  
2. Columns Drop, Mostly fluid, Layout Shfit 
### Day 64: November 9, 2017    

**Today's Progress**:   
1. Today I continued with Udacity's Responsive Web Design Course.  

**Thoughts**:     
1. I've learnt about media queries, breakpoints and flex properties.  
2. It important design mobile first and then add media queires using min-width.  
3. Flex properties: 
```css
  display: flex;
  flex-wrap: wrap;
```
4. `order` Property specify the order of element inside the flex container.  
### Day 63: November 8, 2017    

**Today's Progress**:   
1. Today I've just chilled, made minimum fixed on my portfolio, and listen[ sintax ](https://syntax.fm/) podcast.  
### Day 62: November 7, 2017    

**Today's Progress**:   
1. Today I made the Pixel Art Maker Project from Google Developer Challenge Scholarship: Front-End Web Dev.

# portfolio
### Day 61: November 6, 2017    

**Today's Progress**:   
1. Today I fixed some on the portfolio.
# portfolio
### Day 60: November 5, 2017    

**Today's Progress**:   
1. Today I started a wikipedia viewer.
2. I've decided to use vue-cli to practice.
3. Fetching the Wikipedia API was a mess.  
4. 
 ```javascript
  methods: {
    findArticles() {
      const endpoint = `https://en.wikipedia.org/w/api.php?format=json&action=query&title=<query>&generator=search&limit=10&prop=pageimages|extracts&pilimit=max&exintro&explaintext&exsentences=1&origin=*&exlimit=max&gsrsearch=${this
        .search}`;
      fetch(endpoint)
        .then(data => data.json())
        .then(data => {
          this.articles = data.query.pages;
          console.log(this.articles);
        });
    }
  }
 ```
# portfolio
### Day 54 -59: October 31-November 4, 2017    

**Today's Progress**:   
1. Today I started my new porfolio.

# rest-api-playlist
This is a repository that follows rest-api-playlist by The Net Ninja
https://www.youtube.com/watch?v=BRdcRFvuqsE&list=PL4cUxeGkcC9jBcybHMTIia56aV21o2cZ8

### Day 53: October 30, 2017    

**Today's Progress**:   
1. Today I finished rest-api-playlist.  

**Thoughts**:     
1. I've learnt How to change the data property. 
### Day 52: October 29, 2017    

**Today's Progress**:   
1. Today I continue rest-api-playlist.  

**Thoughts**:     
1. I've learnt How to change the data property. 
2.
 ```javascript
 methods: {
                handleSubmit: function (e) {

                    const lng = this.$refs.lng.value;
                    const lat = this.$refs.lat.value;
                    const endpoint = `/api/ninjas?lng=${lng}&lat=${lat}`;

                    fetch(endpoint)
                        .then(data => data.json())
                        .then(data => {
                            this.ninjas = data;
                        });
                }
            }
```
### Day 51: October 28, 2017    

**Today's Progress**:   
1. Today I continue rest-api-playlist.  

**Thoughts**:     
1. Added Front End to the API suing Vue JS

### Day 50: October 26, 2017    

**Today's Progress**:   
1. Today I continue rest-api-playlist.  

**Thoughts**:     
1. Handling GET requests.
2. New GeoSchema using GeoJson http://http://geojson.org/.  
3. `req.query.lng` return the `lng=` param at the url.  
### Day 49: October 25, 2017    

**Today's Progress**:   
1. Today I continue rest-api-playlist.  

**Thoughts**:     
1. Error handling with a middleware.  `catch()` Promise.
2. Delete and Update using mongoose methods `findByIdAndRemove()`, `findByIdAndUpdate()` and `findOne()`.
3. `req.params.id` to get the id from the address bar.  
4. `req.body` to get the object sent.  
### Day 48: October 24, 2017    

**Today's Progress**:   
1. Today I continue rest-api-playlist.  

**Thoughts**:     
1. `import` and  `export` from ES6 has not support in NodeJS.  
2. https://www.npmjs.com/package/import-export This module can help with  it.  
3. Mongoose: object modeling tool designed to work in an asynchronous environment.
4. Schema and Model.
```javascript
//model
const mongoose = require("mongoose");
const Schema = mongoose.Schema;

//create a ninja Schema and Model
const NinjaSchema = new Schema({
  name: {
    type: String,
    required: [true, "Name field is required"]
  },
  rank: {
    type: String
  },
  available: {
    type: Boolean,
    default: false
  }
  //add in geo location
});
//Model from a Schema
const Ninja = mongoose.model("ninja", NinjaSchema);

module.exports = Ninja;
```  
5. Connect to MongoDB and change the promise (MongoDB Promise is deprecated).  
```javascript
 mongoose.connect("mongodb://localhost/ninjago");
mongoose.Promise = global.Promise;
```
6. Add an object to the Database
```javascript
const Ninja = require("../models/ninja");
//add a new ninja to the database
router.post("/ninjas", (req, res) => {
  Ninja.create(req.body).then(ninja => {
    res.send(ninja);
  });
});
// var ninja = new Ninja(req.body);
// ninja.save();
```
### Day 47: October 23, 2017    

**Today's Progress**:   
1. Today I continue my app for countries information.  

**Thoughts**:     
1. It works!
2. https://josewhitetower.github.io/list-of-countries/
### Day 46: October 22, 2017    

**Today's Progress**:   
1. Today I started my app for countries information.  

**Thoughts**:     
1. API : https://restcountries.eu/rest/v2/all
2. Fetch the API.  
```javascript
   function getAllCountries() {
            const endpoint = 'https://restcountries.eu/rest/v2/all';
            fetch(endpoint)
                .then(blob => blob.json())
                .then(countries => {
                    select.innerHTML += countries.map(d => `<option value="${d.name}">${d.name}</option>`);
                });

        }
```
3. Asynchronous method invocation.  https://en.wikipedia.org/wiki/Asynchronous_method_invocation
### Day 45: October 21, 2017    

**Today's Progress**:   
1. Today I startet  with rest-api-playlist.  

**Thoughts**:     
1. `npm init -y`: create a package.json an autocompletes.  
2.  HTTP Methods: GET, POST, PUT and DELETE.  
3. Set up and express app.  
```javascript
const express = require("express");
const app = express();
  //listen for requests
app.listen(process.env.port || 4000, function() {
  console.log("now listening for requests");
});
``` 
4. Handle GET Requests.  
```javascript
// handling get requests
app.get("/api", function(req, res) {
  console.log("GET request");
  // res.end();
  res.send({ name: "Yoshi" });
});
```
5. Router
```javascript
//api.js
const express = require("express");
const router = express.Router();

// get the list of ninjas from the database
router.get("/ninjas", function(req, res) {
  res.send({ type: "GET" });
});
module.exports = router;
```
```javascript
//index.js
const routes = require("./routes/api");
const app = express();

//initialize routes
app.use("/api", routes);
```
# javascript30
This is a repository that follows Javascript30 by @wesbos 
https://javascript30.com/ 
### Day 44: October 20, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. `e.isTrusted`: The isTrusted event property returns a Boolean value indicating whether the event is trusted or not.  
2. Note: In Chrome, Firefox and Opera, the event is trusted if it is invoked by the user, and not trusted if it is invoked by a script. In IE, all events are trusted except those that are created with the createEvent() method. 
### Day 43: October 19, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. `clearInterval()`:The clearInterval() method clears a timer set with the setInterval() method.  
2. `document.title `: Set the title of the tab bar(document).  
3. Working with dates.
```javascript
  function displayEndTime(timestamp) {
  const end = new Date(timestamp);
  const hour = end.getHours();
  const mins = end.getMinutes();
  endTime.textContent = `Be back at ${hour}:${mins < 10 ? "0" : ""}${mins}`;
}
```
4. ` this.reset()` to clear a formular.  
### Day 42: October 17, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. `video.playbackRate`:sets or returns the current playback speed of the audio/video.  
2.  Rate: `const playbackRate = percent * (max - min) + min;`
### Day 41: October 16, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. `event.pageX`: Return the position of the mouse pointer.
2. `scrollLeft` & `scrollTop` Properties.
```javascript
let elmnt = document.getElementById("myDIV");
let x = elmnt.scrollLeft;
let y = elmnt.scrollTop;
```

### Day 40: October 15, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Element coordenates.
```javascript
      const dropdownCoords = dropdown.getBoundingClientRect();
```
2. Set Element's property.  
```javascript
        background.style.setProperty('width', `${coords.width}px`);
```
3. Time out function and inline `if` as lambda function.   
```javascript
  setTimeout(() => this.classList.contains('trigger-enter')
        && this.classList.add('trigger-enter-active'), 150);
```
### Day 39: October 14, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Event Capturing.
```javascript
  divs.forEach(div => div.addEventListener('click', logText, {
      capture: true, //tit will only add the event listener to this element and not to its parents
      once: true // to execute only once
    }));
```
2. Stop bubbling.  
```javascript
  function logText(e) {
      console.log(this.classList.value);
      // e.stopPropagation(); // stop bubbling!
      // console.log(this);
    }
```
### Day 38: October 13, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Change event from an element.
```javascript
   voicesDropdown.addEventListener('change', setVoices);
    //voicesDropdown.onchange = setVoice  
```
2. Call a function and pass a parameter.
 ```javascript
    stopButton.addEventListener('click', () => toggle(false));
    stopButton.addEventListener('click', toggle.bind(null, false));
    stopButton.addEventListener('click', function () {
      toggle(false)
    });
```
3. `window.scrollY` to know where the windows is.  
4. `element.offsetHeight + 'px'` to know the height of the element.  
5. `element.offsetTop + 'px'` to know the top position of the element.  
6. window's event scroll
``` javascript
    window.addEventListener('scroll', fixNav)
```   
### Day 37: October 12, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Follow along links.  
2. How to get the element coordinates.  
3. Build an object and read its properties.  
4. CSS property: transform.  
 ```javascript
    const linkCoords = this.getBoundingClientRect()
        const coords = {
        width: linkCoords.width,
        height: linkCoords.height,
        top: linkCoords.top + window.scrollY,
        left: linkCoords.left + window.scrollX
      };
      highlight.style.height = `${coords.height}px`;
      highlight.style.width = `${coords.width}px`;
      highlight.style.transform = `translate(${coords.left}px,${coords.top}px)`
    }
    triggers.forEach(a => a.addEventListener('mouseenter', highlightLink))
  
```
### Day 36: October 11, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Device Orientation and Navigator Geolocation.  
 ```javascript
      navigator.geolocation.watchPosition((data) => {
      console.log(data);
    }, (err) => {
      console.error(err);
      alert('HEY! YOU GOTTA ALLOW THAT TO HAPPEN!!!');
    });

    if (window.DeviceOrientationEvent) {
      window.addEventListener('deviceorientation', deviceOrientationHandler, false);
    }
```
### Day 35: October 10, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Speech recognition.  
 ```javascript
  window.SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
    const recognition = new SpeechRecognition();
    recognition.interimResults = true;
```

### Day 34: October 9, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Video
 ```javascript
function getVideo() {
  navigator.mediaDevices.getUserMedia({ video: true, audio: false })
    .then(localMediaStream => {
      console.log(localMediaStream);
      video.src = window.URL.createObjectURL(localMediaStream);
      video.play();
    })
    .catch(err => {
      console.error(`OH NO!!!`, err);
    });
}
```

### Day 33: October 8, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. 
### Day 32: October 7, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Use `e.offsetY` and `e.offsetY` to get the position where he cursor is.
2. `String.prototype.trim()` returns a  new string representing the calling string stripped of whitespace from both ends.
### Day 31: October 5, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Today I made toggleAll on Local Tapas 
### Day 30: October 4, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Asigning values to strings, numbers or booleans copies will not tu update the orginial value.  
2. Doing it to Array or Objects will. They are not copies, but references.  
3. `e.preventDefault` prevent the page to reload.  
4. `JSON.stringify()`  and `JSON.parse()` Objects to Strings and viceversa.  
5.  Event delegation allows you to avoid adding event listeners to specific nodes;  instead, the event listener is added to one parent.  
6. Using the Element.matches API, we can see if the element matches our desired target.  
### Day 29: October 3, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Key Sequence Detection.  
2. Slide In on Scroll.  
### Day 28: October 1, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Dev Toll Tricks `console.time`, `console.count`, `console.clear`,`console.group`, `console.dir`, `console, assert`, `console.info`, `console.warn`, `console.error`.  
2. Muiltiple checkboxes. 
3. HTML5 Video Player.  
### Day 27: September 28, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Canvas methods
### Day 26: September 27, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Array methods `Array.prototype.some()`, ` Array.prototype.every()`, `Array.prototype.find()` , `Array.prototype.findIndex()`.  
### Day 25: September 26, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. `fetch(endpoint).then(blob=>blob.json()).then(data=> cities.push(...data))` to put the JSON elements into arrays.  
2. `const regex = new RegExp(wordToMatch, 'gi');` to create a Regular expression.  
### Day 24: September 25, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. toggleOpen will not be excetuted when the document load, toggleOpen() will.  
### Day 23: September 22, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Array methods `filter`, `map`, `sort`, `reduce`.  
2. `console.table()`  
### Day 22: September 21, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. Variables CSS `:root{--name:value}`.  
2. Access to variable `var(--name)`. 
3. Events `change` `mousemove`.
4. HTMLElement.dataset property allows access, both in reading and writing mode, to all the custom data attributes (data-*) set on the element, either in HTML or in the DOM.  
### Day 21: September 20, 2017    

**Today's Progress**:   
1. Today I continued with JavaScript30.  

**Thoughts**:     
1. `transform-origin` by defautl 50%, allows to pivot the element at all.  
2. `transform` allows you to rotate, scale, move, skew, etc., elements.  
3. `transition` allows you to change property values smoothly (from one value to another), over a given duration. `transition-timing-function` https://www.w3schools.com/css/css3_transitions.asp.  

### Day 20: September 19, 2017    

**Today's Progress**:   
1. Today I started with JavaScript30.  

**Thoughts**:     
1. `document.querySelector` returns the first element that matches a specified CSS selector(s) in the document.  
2. `e.propertyName` returns the name of the CSS property associated with the transition, when a transitionevent occurs. This property is read-only.  


# CSS Flexbox-playlist log
### Day 19: September 17, 2017    

**Today's Progress**:   
1. Today I learnt about Axis, `flex-flow` to set the direction.  

**Thoughts**:     
1. `flex-flow` by default is `row`. 
2. `justify-content` only works in the main axis.   
3. `align-items` only works in the cross axis.  
4. `box-sizing:border-box` is used to tell the browser what the sizing properties (width and height) should include. `content-box` by default.  
### Day 18: September 16, 2017    

**Today's Progress**:   
1. Today I learnt about Nested Menus with flexbox.   

**Thoughts**:     
1. 
### Day 17: September 15, 2017    

**Today's Progress**:   
1. Today I learnt about Flex wrap.  
2. Create a menu with the property `justify-content`.  

**Thoughts**:     
1. The container must have the property `flex-flow:wrap` it makes it responsive.    
### Day 16: September 13, 2017    

**Today's Progress**:   
1. Today I learnt about Flex shrink.  

**Thoughts**:     
1. `flex-shrink:[value]` used to shrink elements into available space in relation to others.  

### Day 15: September 12, 2017    

**Today's Progress**:   
1. Today I learnt about Flex grow.  

**Thoughts**:     
1. `flex-grow:[value]` used to expand elements into available space

### Day 14: September 11, 2017    

**Today's Progress**:   
1. Today I learnt about Flex containers. 

**Thoughts**:     
1. A container should have the property `display:flex` and then the elements inside will have the flex behavios

# CSS Positioning-playlist log

### Day 13: September 10, 2017    

**Today's Progress**:   
1. Today I learnt about Floating Columns.  
2. Text columns.  
3. Postion Relative.  
4. Fixed Position.  
 

**Thoughts**:     
1. `float: left; width: 46%;` to divide it in two columns.  
2. `column-count, column-gap, column-rule` to separate the columns.  
3. When `position:relative` is set, you can offset the elements witht `left, right, top, bottom`.  I will keep the element in normal document flow
4. `position:absolute` will remove an element from the normal document flow. It's position will be absolute compare to its closest relative parent element. 
5.`position:fixed` Always is relative to the document window. Will remove an element from the normal document flow. 

### Day 12: September 9, 2017    

**Today's Progress**:   
1. Today I learnt about CSS Positioning.  
2. Normal document flow.   
3. Floating elements.  
4. Clearing Floats.  
 

**Thoughts**:     
1. `display:inline-block` makes the inline elements like `a or span` to behave like blocks elements like `p or div`.  
2.  `line-height` defines the height of the line in a text, the space between lines.  
3. The `float` property is makes an element to break the normal document flow. No longer occupy a hight.  
4. The `margin`, `padding` should be taken cared when we use the `width` and `height`.  
5.  The `clear`  property restore the normal document flow. It has to be placed at the end of the element.   
6. Take a look at the `:after{content:"";display:block; clear:both}` rule.  

# JavaScript ES6-playlist log

983e93590a171d19032c8823868f8bcb0d21fe6c
### Day 10: September 6, 2017    

**Today's Progress**:   
1. Today I learnt about Responsive Images.  
 

**Thoughts**:     
1. Pollyfills. Library to use the tag `picture` on IE.  
### Day 9: September 5, 2017    

**Today's Progress**:   
1. Today I learnt about Media Queries.  
2. Fluid vs Fixed Layouts.  

**Thoughts**:     
1.  Use relatives measures -> porcentual values.  
### Day 8: September 4, 2017    

**Today's Progress**:   
1. Today I learnt about Sets.  
2. Methdos `add`, `delete` ,`size`, `clear`, `has`.  
2. Responsive Design  

**Thoughts**:     
1.  `ninjas=[...refindeNinas]` spread the array ninjas equals to the Set refinedNinjas into individuals components.      
2. `var refinedNinjas= new Set(ninjas)` define a set with the calues of the array (uniques).  
3. The viewport Tag `viewport`

### Day 7: September 3, 2017    

**Today's Progress**:   
1. Today I learnt how to make a feature request on another project

**Thoughts**:     
1.  it was closed :(  
### Day 6: September 2, 2017    

**Today's Progress**:   
1. Today I learnt about the spread operator.  
2. Template string `console.log(`my name is ${name} and my age is ${10+9}`);
3. Object Literal Enhancemnts  
4. New Strings methods
5. Arrow Functions

**Thoughts**:     
1.  If you use the arrow function, you don't lose the scope of the variables. You don't need to create a reference to the variable (_this) to keep the scope.  

**Link to work:**:     
1. [Example](https://link) 
### Day 5: September 1, 2017    

**Today's Progress**:   
1. Today I learnt how to declare and use a constant, let, default params

**Thoughts**:     
1.   

**Link to work:**:     
1. [Example](https://link) 

# Grunt-playlist log
### Day 4: August 31, 2017    

**Today's Progress**:   
1. Today I learnt how to install grunt-cli and grunt.  
2. How to load a pluging (concatenating files) and how to register a task to run certain parts of the plugin.

**Thoughts**:     
1. I must install grunt with the npm and as option "--save-dev" to save it as devDependencies.  
2. The grunt file must be a module, and it should be exported (module.exports= function(grunt){}).  

**Link to work:**:     
1. [Example](https://link)

sass-playlist

# SASS Playlist - Log

### Day 3: August 30, 2017    

**Today's Progress**:   
1. Today I learnt how to create a grid using math operators and mixins.  
2. Colour functions  
3. The @Content Keyword  
4. If Statements

**Thoughts**:     
1. There's a math form, the operators need to be separated by space.  
2. Remeber, you can pass parameters to the mixins.  
3. [Here](http://sass-lang.com/documentation/Sass/Script/Functions.html) you can find the Functions reference  
4. The @content keyword allows to a mixin that you can use everywhere, with params you can define it as you like and it will take that to the mixin that contains the @content keyword  
5. If you dont know how many params a function will have you can use ($arg...) as parameters, it will generate a list, and you can find the length of this list unsing the function length().

**Link to work:**:     
1. [Example](https://link)  
### Day 2: August 29, 2017    

**Today's Progress**:   
1. Today I learnt about mathematical operators  

**Thoughts**:     
1. Just to adjust the width of elements?.    

**Link to work:**:     
1. [Example](https://link)  
### Day 1: August 28, 2017    

**Today's Progress**:   
1. Today I learnt about mixins and how to import files.  
2. There is an option in Prepros, that allows to autompile or not the .saas files. You must have only one file to compile, the rest should be imported in the last one.  
3. Pseudo Classes and How to import a mixin (that's included in a mixin.scss file) -> @include [name_of_the_mixin]  

**Thoughts**:     
1. Surprisely the style worked fine, not like the night before.    

**Link to work:**:     
1. [Example](https://link)
### Day 0: August 27, 2017  
Introduction to SAAS  
**Today's Progress**:   
1. I installed SASS on my computer using [Prepros](https://prepros.io/downloads) A tool to compile sass files to css and visualize live reload changes  
2. I learned how to declare SASS variables and nest them.  

**Thoughts**:    
1. It was a lit bit complicated to see it like in the video. I just noticed that there are some differences between the files in the video and the git repostiory. I had to add a link to the reset.css file.  

**Link to work**:     
1. [Example](https://link)
