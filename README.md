osc.js
======

osc.js is a library for reading and writing [Open Sound Control](http://opensoundcontrol.org) messages in JavaScript. It has no dependencies on the type of environment or transport used. As a result, it works both in Node.js and in a web browser.

Why osc.js?
-----------

There are several other OSC libraries available for JavaScript. However, they all depend on Node.js-specific APIs. This means that they can't be run in a browser. osc.js uses only cross-platform APIs (specifically, `TypedArrays` and `DataView`), ensuring that it can run in any modern JavaScript environment.

What Does it Do?
----------------

osc.js reads and writes OSC-formatted binary data into plain JavaScript objects. It provides adaptors for Node.js Buffer objects as well as standard ArrayBuffer objects.

You can receive OSC data in whatever manner works best for your application: serial port APIs such as node-serialport or chrome.serial, socket APIs such as Node.js dgram or WebRTC data channels, WebSockets or binary XHR messages should all work. Connect osc.js up to your source of incoming/outgoing data, and you're all set.

This approach is consistent with the design of Open Sound Control as a _content format_ that is independent from its means of transport.

Status
------

osc.js is still under development. It supports all OSC 1.0 and 1.1 required types, and most optional types. The semantics for time tags conform to the OSC 1.0 specification.

osc.js does not yet (but will) support:

* color types
* MIDI types
* array types ("[" and "]")
* documentation
