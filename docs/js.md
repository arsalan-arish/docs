# JavaScript  

## Data types  
### Primitives  
number  
string  
boolean  
bigint  
symbol  
null  
undefined
### Non-Primitives  
object  
array  
function  

Everything is an object (stored in heap memory) except primitive values. Primitives (stored in faster memory regions like stack, though not the concern of JS programmer) are immutable, they cannot be modified. Though, the variables pointing to immutable primitives can be reassigned to get the illusion of modification. JS uses 'autoboxing' when methods are called on primitive values, which wraps them in objects temporarily.

Only an object is a non-primitive, functions and arrays are actually objects with key-value pairs under the hood. Object is mutable, and variables only store reference to them. The primitives are also available in object form, but note that their underlying raw values are still immutable

All variables are hoisted by the JS Engine before the code execution actually starts:  
- 'var' ones are initialized with 'undefined' type, irrespective of the scope.  
- 'let' ones are not initialized.  
- 'const' are just like 'let' except that they cannot be reassigned once assigned with declaration  
- functions declared with 'function' keyword and a name are initialized properly with their bodies  
- anonymous functions with no name (arrow notation or 'function' kw) that are assigned to variables are initialized (assigned) accordingly with the 'var', 'let', or 'const' keyword of the variable  

## Execution order of a browser

Once a browser is returned the HTML file on its GET request, it starts parsing it and building the DOM. Any link, img, icon tags in the middle are ignored for later. Only script tags are considered:  

- In a normal script tag, the browser blocks HTML parsing, downloads the script by sending a GET request to its src, executes the script fully, and then continues parsing HTML. Note that the download time acts as a bottleneck  
- In a 'defer' script tag, the browser ignores the script tag just like others for later.  
- In a 'async' script tag, the browser asynchronously triggers the script download while keeps parsing HTML. The moment the script downloads, it stops (blocks) parsing, executes the script, then continues parsing.

Once parsing HTML and building DOM is complete:  

1. It executes the 'defer' scripts.  
2. It fires 'DOMCompleteLoaded' event (on document).   
3. It downloads from the src of all the other css, img, icon, etc... tags, also builds CSSOM.  
4. It builds the render tree from the DOM and CSSOM, and paints the screen UI visible.  
5. It fires the 'load' event (on document).


Then JS Event Loop takes control. In each iteration of the event loop:  

1. It makes sure the call stack is empty. It would be empty because at this point all the JS scripts have executed, except that a user given console command can fill it back. Also if a script tag is dynamically added to the DOM, it will trigger its execution, filling the call stack  
2. It executes all the tasks in the Microtask queue, which contains resolved promises, etc..  
3. It executes one task in the Task (or Macrotask) queue, which contains function callbacks, etc..  
4. It updates the UI thread, which includes processing events, painting the next frame, syncing the UI with the DOM (if modified), etc..  

This is it. The event loop continues forever so that the website remains responsive. If the user tries to close the tab:  

- **beforeunload** (The "Are you sure?" Event):  

This fires immediately before the page begins to unload. Its primary purpose is to allow you to trigger a confirmation dialog asking the user if they want to leave. When it works:
  - Closing the browser tab or the entire window.
  - Clicking a link that takes the user to a completely different website in the same tab.
  - Clicking the browser's Refresh/Reload button.
  - Clicking the browser's Back or Forward navigation buttons.
  - Submitting an HTML form that redirects to a new page.
  - Programmatically changing the location via JavaScript (window.location.href = ...).

---
- **unload** (The "Clean Up" Event):  

This fires after beforeunload has finished, only after the user has confirmed they want to leave (if a beforeunload prompt was shown). 

  - Crucial Modern Warning: Modern browsers aggressively restrict what you can do in unload. You cannot show alerts, and network requests will be aborted unless you use navigator.sendBeacon(). In fact, modern Chrome is actively phasing out the unload event entirely because it hurts performance

---

