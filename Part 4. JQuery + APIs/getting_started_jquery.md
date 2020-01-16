# Getting Started

To get started with jQuery, go to [Microsoft's jQuery Releases on the CDN](https://docs.microsoft.com/en-us/aspnet/ajax/cdn/overview#jQuery_Releases_on_the_CDN_0) and copy the link from there. This is the address we will tell our browser to import the library from. Next, in the **`<head>`** portion of your HTML document, include the link you just copied:

`<script src="https://ajax.aspnetcdn.com/ajax/jquery/jquery-1.9.0.js"></script>`

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


#### NEXT: [Getters and Setters](./getters_setters.md)
