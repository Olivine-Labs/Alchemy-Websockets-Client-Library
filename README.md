Alchemy Websockets
=============

A websocket server built in C# to be extremely efficient and scalable over high 
numbers of connections.

It follows most jslint / gjslint conventions.

Usage
-------
Include the javascript as a reference. Starting a server is as simple 
as instantiating a server object, opening the connection, and binding events.

An example application can be seen on [alchemy-websockets-example](https://github.com/Olivine-Labs/Alchemy-Websockets-Example)

Example:

	// Set up the Alchemy client object
	AlchemyChatServer = new Alchemy({ 
		Server: "olivinelabs.com",
		Action: "chat",
		DebugMode: false
	});
	
	AlchemyChatServer.Connected = function(){
		console.log("connected");
	};
	
	AlchemyChatServer.Disconnected = function(){
		console.log("disconnected");
	};
	
	AlchemyChatServer.MessageReceived = function(event){
		ParseResponse(event.data);
	};
	
	AlchemyChatServer.Start()


License
-------
MIT
Copyright (C) 2011 Olivine Labs, LLC

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.