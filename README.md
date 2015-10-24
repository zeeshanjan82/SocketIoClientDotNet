# SocketIoClientDotNet
====================

Socket.IO Client Library for .Net

This is the Socket.IO Client Library for C#, which is ported from the [JavaScript client](https://github.com/Automattic/socket.io-client).

See also: [EngineIoClientDotNet](https://github.com/Quobject/EngineIoClientDotNet)

## Installation
[Nuget install](https://www.nuget.org/packages/SocketIoClientDotNet/):
```
Install-Package SocketIoClientDotNet
```

## Usage
SocketIoClientDotNet has a similar api to those of the [JavaScript client](https://github.com/Automattic/socket.io-client).

```cs
using Quobject.SocketIoClientDotNet.Client;

var socket = IO.Socket("http://localhost");
socket.On(Socket.EVENT_CONNECT, () =>
{
	socket.Emit("hi");
	
});

socket.On("hi", (data) =>
	{
		Console.WriteLine(data);
		socket.Disconnect();
	});
Console.ReadLine();
```

More examples can be found in [unit tests](https://github.com/Quobject/SocketIoClientDotNet/blob/master/Src/SocketIoClientDotNet.Tests.net45/ClientTests/ServerConnectionTest.cs) acting against the [test server](https://github.com/Quobject/SocketIoClientDotNet/blob/master/TestServer/server.js).

## Features
This library supports all of the features the JS client does, including events, options and upgrading transport.

## Framework Versions
.Net Framework 3.5, .Net Framework 4.0, .Net Framework 4.5, Windows 8, Windows 8.1, Windows Phone 8, Windows Phone 8.1, Mono, Unity3D, Xamarin-iOS,  Xamarin-MonoTouch,  Xamarin-Android

## License

[MIT](http://opensource.org/licenses/MIT)

## Say Hi
Please find more on me at www.zeeshanjan.com
