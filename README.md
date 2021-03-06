TiMessageTableViewController
============================

This is a wrapper module for [MessagesTableViewController](https://github.com/jessesquires/MessagesTableViewController) on Titanium Mobile.

GET STARTED
------------

REGISTER THIS MODULE
---------------------

Register this module with your application by editing `tiapp.xml` and adding this module.
Example:

```
<modules>
  <module version="0.1" platform="iphone">com.arihiro.messagestable</module>
</modules>
```

When you run your project, the compiler will know automatically compile in your module
dependencies and copy appropriate image assets into the application.

USING THIS MODULE IN CODE
-------------------------

To use this module in code, you will need to require it.

For example,

```
var TiMessagesTableViewController = require('com.arihiro.messagestable');

// create view with options
var view = TiMessagesTableViewController.createView({
  height: 480, width: 320, backgroundColor: '#ddd',
  placeHolder: 'Please input message!', sender: 'ari_hiro',
  incomingBackgroundColor: '#88E', outgoingBackgroundColor: "#E88",
  incomingColor: '#115', outgoingColor: "#511",
  senderColor: '#222', timestampColor: '#555'
});

// send message
view.sendMessage({text: 'Ho-ge Ho-ge', sender: 'hiro_ari', date: new Date()});
```

HANDLE EVENTS
-------------

```
view.addEventListener('opened', function(e) { console.log(e); }); // view is opened
view.addEventListener('closed', function(e) { console.log(e); }); // view is closed
view.addEventListener('showinput', function(e) { console.log(e); }); // message input view is hidden
view.addEventListener('hideinput', function(e) { console.log(e); }); // message input view is shown
view.addEventListener('send', function(e) { console.log(e); }); // send a message
view.addEventListener('click', function(e) { console.log(e); }); // click list of messages view
```

Cheers!
