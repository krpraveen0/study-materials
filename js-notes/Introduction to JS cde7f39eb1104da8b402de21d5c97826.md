# Introduction to JS

What is Javascript?

Javascript is a functional, object based scripting language. Initially Javascript was created to make web page alive.

It doesn't need compilation we can simply write our script and run it directly in the browser.

Javascript code is converted into machine level code by using an interpreter which is already available in all browser.

Why the name is JavaScript?

When js was created, it had another name ie "LiveScript". But at that time Java was very popular, so it was decided that positioning a new language as a "younger brother" of Java would help Javascript to grow.

With time as it evolved, JS became a fully independent language with its own specification called **ECMAScript,**  and now JS has no relation to Java at all.

Today not only we can use JS in the browser but also on the server or actually on any device which has special program called **Javascript Engine.**

![JS-Engine.png](Introduction%20to%20JS%20cde7f39eb1104da8b402de21d5c97826/JS-Engine.png)

Every browser has an embedded engine with it sometimes we call it as "Javascript virtual machine".

Different browser has different JS engine having different code name ie :

1.) V8 - in Chrome and Opera.

2.) SpiderMonkey - in FireFox

3.) Chakra - in IE

4.) SquirrelFish - Safari etc

**How the JS Engine Work?**

The working of JS Engine is quite complicated but to understand in basic following steps

1. The engine(embedded if it's a browser) reads(parses) the scripts.
2. Then it converts ("interpretes") the script to the machine language.
3. Finally machine code is run .

Now the JS engine applies several optimizations at each step of the process. It even watches the compiled script as it runs, and analyze the data that flows through it, and further optimizes the machine code based on that analysis.

**What Javascript can do in browser**

JS doesn't provide low-level access to memory or CPU, because it was initially created only for browsers which doesn't requires those features.

JS capabilities greatly depends on the environment in which it is running. Just for an example

Node.js supports functions that allows JS to read/write an arbitrary files or perform network requests etc.

In browser JS can do everything related to webpage manipulation, interaction with the user and the webserver. so in browser JS is capable to do following things:

1. It can add new html to the page ,change the existing content and modifing the styles.
2. It can be used to react to user interaction, run on mouse clicks, pointer movements, key press.
3. Send request over the network to remote server, download and upload files(so-called AJAX or COMET Technologies)
4. We also use JS script to get and set cookies,ask questions to the visitor, show messages.
5. JS is also used to remember data on the client-side using local storage feature of the browser.

**What JS can't do in the browser**

JS abilities in the browser is limited for the sake of user's safety. So that webpage cannot access our private information or harm our local system data.

Some of the restrictions on JS in browser are:

1. JS on a webpage cannot read/write arbirary files on the harddisk, copy them or execute a programs . It has no direct access to any os functions.

NOTE: Modern browsers allows JS to work with files, but the access is limited and only provided if the user does certain actions  like "dropping" a file in the browser area or selecting a file via input tag.

Moreover there are ways to interact with camera/microphone and other devices, but they again require a user's explicit permission. So a JS-enabled page may not instantaneously enable a web-camera, observe the surrounding and send the information to the third party .

1. Different tab/windows of browser generally do not know about each other. Sometimes they do know, for example when one window uses JS to open the other page. But even in this case JS from one page may not access the other if they come from different sites (from different domain, protocol or port). This is called "Same Origin Policy" .Now to work around those pages, both pages must agree for the data exchange and contain a special JS code that handles it.

What makes js unique?

Some thing which makes JS unique are:

1. JS provides full integration with HTML/CSS.
2. In JS simple things are done simply.
3. It is supported by all major browsers and enabled by default.