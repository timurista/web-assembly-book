# What is Web Assembly

To understand what web assembly is, you need to see the history of web assembly in the context of the overall web lifecycle for a typical browser.

First, the browser makes a series of http requests to a given server, that server returns in it's response various entities including the html page, perhaps some requested css or javascript files as the html is being parsed. Once the website has been loaded, or the DOM has been instantiated, then various ohter assets are loaded, and javascript is parsed, compiled and interpreted. The typical delivery method for getting logic into an application so it can do dynamic things on the client is to either a\) use javascript file which has support in the html document and can grab and parse information, or b\) use the server by sending a request and grabbing the response. Javascript compilation and execution has been highly optimized over the past few years, but there is an upper limit to how good javascript or any dynamic language can perform simply because it must be compiled and executed at runtime.

Web assembly is a way to shortcircuit the inherint limitation of javascript and feed the DOM and your brwoser some binary or near machine code representation which can interact at a low level with the host machine. This means that for graphics intensive applications, it will become possible to make your application run fast, really really fast.

However, the tradeoff is that you have to ship a web assembly file named \(wasm\) which contains the computational power you need and then import it during the javascript execution timeline. In Chapter 2 we will talk about specifically how to do this with the current api for javascript. But for now, just know that the compiled web assembly module can be accessed in hte global window object through the WebAssembly class with it's own streaming methods and protocols.



Note executed in sandbox environment in web browser after a verification step



