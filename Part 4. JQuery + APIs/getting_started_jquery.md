# Getting Started

To get started with jQuery, go to [google's hosted jQuery library](https://developers.google.com/speed/libraries/#libraries) and copy the link from there. This is the address we will tell our browser to import the library from. Next, in the **`<head>`** portion of your HTML document, include the link you just copied:

`<script src= 'http://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js'></script>
`
Notice that what we are doing is adding a **'source' attribute** to our JavaScript. We are effectively telling our page: "take all the code hosted at this URL and allow me to use it on this page." **Also, notice we added an http:// in front of the URL. You must do this!!!**

Next, open a new **`<script>`** tag and type the following:

`console.log($)`

The `$` is how we access the whole jQuery library. Everything we do with jQuery has to be preceded by a `$`. Next, you can utilize jQuery by adding () to the end of our `$`.

`console.log($())`

The `$()` is how we select an HTML tag. If we were to select the tag, we would have to write `$('body')`. This selector can grab any HTML tag, we will go into the different ways we can grab HTML items.

```
$('body').click(function(){
    // more code will go here
});
```

```
$(document).ready(function(){
 });
```
Inside the curly brackets of the function above is where you are to insert **all** of the jQuery functions. This code tells the browser to execute the jQuery functions when the document itself is ready. By _'ready'_, we mean when the document is fully loaded. This is **very important** because if you don't use this **`ready()`** function, your code will run before the HTML content you wrote gets rendered--meaning, the browser will run code for HTML that doesn't exist yet.

# JQuery Basics

Once you have your jQuery library linked to your page and your **`$(document).ready()`** is set, you are now ready to get going!

There are three portions for using jQuery. The first is the selector which is **`$('body')`**. The selector syntax works exactly like the CSS selector syntax except that everything goes inside of this: **`$(' ')`**. This is how we grab an HTML item. Here are some examples of how to select an HTML item.

###### Don't forget: all must go within your `document.ready()` tags!

#### Select the HTML element/class/id:

So in order to select all of the buttons of your web page, you type:

```$('button')```

That's it! Now you can add all sorts of cool functional properties to your buttons. What if you want to select all buttons with class name _blue_? Same as CSS!:

```$('button.blue')```

Easy! Now, if you want to select all buttons AND elements with class _blue_, do the following:

```$('button, .blue')```

And if you want to select an HTML with an ID, here is how we do that.

```$('#red')```

There you have the jQuery selector!

#### Add an event handler

Now that we have selected something using the jQuery selector, we can add an event listener. Remember, jQuery and JavaScript make a website interactive, and this is how we define what happens to those interactions. An **Event listener** is a trigger for all the code we wish to write that involves the element we selected. The event listener for a button being clicked:

```$('button').click();  //now the document is listening on a click event for the button element!```

Now, we have made jQuery listen for any button to get clicked. We have set an event listener for all buttons using jQuery.

#### Write the action!

The last portion is the action we want our page to enact when this event is triggered. So what happens now? What happens when we click a button on our page? Nothing yet because we haven't coded what we want to happen! Well, let's make something happen, let's add an action.

```
$('button').click(function(){
    alert("You have clicked a button!");
 });
```

Now, when you click a button on your webpage, you should see a pop up with the message we inserted. We put the **`function(){}`** code in to tell jQuery that we want to run a function when the button is clicked. Within that function, we write the code that makes the website interactive! If we want to pass parameters to the function, we specify them in the parenthesis. That's it! This is how you begin to incorporate jQuery into your websites. Take a few minutes to review the syntax for this function, as there are lots of parenthesis and brackets to account for.

### **Keep in mind the basic flow of using jQuery:**

1. **Select the _element, class_ or _id_ using the jQuery selector.**
2. **Add an event listener: How do you want this event to be triggered?**
3. **Write the code on what you want to happen when the event is triggered.**

# What is jQuery?
jQuery is a JavaScript library. What this means for us is that it allows every browser to read JavaScript code. In the same manner, browser compatibility is a big issue when working on the front-end. This means that the jQuery code you write is suited for use by all browsers without change. JavaScript is interpreted by your browser, and unfortunately, Google Chrome interprets JavaScript differently than Safari, Mozilla and Internet Explorer do.  We don't want to have to write different versions of our code for different browsers, so cross-browser compatibility is important. All of the jQuery's functions work the same way regardless of which browser the user is running.

JQuery also converts what would have been a long block of code into just a few lines. As a developer, you should always practice the DRY method (Don't Repeat Yourself) which a group of developers discovered when they wrote the same lines of code over and over again (and it was a good amount of code too!). So, why not cut down many lines of code by making a library, and also by simplifying it for everyone? It sounds like a great idea!

# Overview of basic jQuery functions and $(this)

To get started with jQuery, go to [google's hosted jQuery library](https://developers.google.com/speed/libraries/#libraries) and copy the link from there. This is the address we will tell our browser to import the library from. Next, in the `<head>` portion of your HTML document, include the link you just copied:

```<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>```

Notice that what we are doing is adding a 'source' attribute to our JavaScript. We are effectively telling our page: "take all the code hosted at this URL and allow me to use it on this page."

List of functions you should get familiar with:

* Effects (functions to do some cool animation effects)
  - .hide()
  - .show()
  - .toggle()
  - .slideUp() - not available in the slim version
  - .slideDown() - not available in the slim version
  - .slideToggle() - not available in the slim version
  - .fadeOut() - not available in the slim version
  - .fadeIn() - not available in the slim version
* CSS (adding or removing a class for any HTML element/DOM)
  - .addClass()
  - .removeClass()
  - .css()
* Manipulation (retrieving or setting value or text in any HTML element)
  - .after()
  - .append()
  - .prepend()
  - .attr()
  - .before()
  - .html()
  - .text()
  - .val()
* Events (functions to handle an event)
  - .click()
  - .hover()


There is more than one way to add JQuery to your project. Some developers put their jQuery codes in the head like this:
```
<head>
<script>
   $(document).ready(function() {
       // your jquery codes here
   });
</script>
</head>
```
Other developers don't want jQuery to wait for the document to be fully ready, and insert their jQuery codes just before the ```<body>``` tag ends.
```
<script>
  // your jquery codes here
</script>
</body>
```
Please make sure you're closing all the open parenthesis and curly brackets in all the appropriate places. Also, use Inspect Element frequently to see if there are any javascript errors in your codes.

## Other tips that may be helpful

You can also use .html or .text to retrieve/get the value.  For example on the bootstrap pricing page

```
var a = $('h1').html()
console.log(a); // would print "Pricing"
```

As you go through the documentation, you can learn more about how the same method could be used to retrieve information (usually if no argument is passed to the method) or to set information (usually by passing some additional information to its method).

You could also grab a specific element by tagging that element with a specific id.  For example, if you had a button with an id of 'btn_fade' that hides all the paragraphs with a class of 'sp', when the button is clicked, you could do:

```
$('#btn_fade').click(function() {
   $('p.sp').hide();
});
```

Please make sure whenever you use jQuery, you're very careful where you open the parenthesis and the curly brackets. Always check Google Inspect's Console to see if it caught any Javascript errors and also add console.log statements within the function to ensure that the browser is even going inside that function when certain events are triggered.

#### NEXT: [Getters and Setters](./getters_setters.md)
