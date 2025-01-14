# Overriding Event Listener in HTML

This repository demonstrates a subtle bug in HTML related to event listeners.  The code includes an example of attaching multiple event listeners to a single element using both `addEventListener` and the `onclick` property. This approach unintentionally overrides the first event listener, resulting in unexpected behavior.  The solution provided shows the correct way to manage multiple event listeners.

## Bug Description

The bug occurs because assigning a new function to the `onclick` property replaces any previously attached listeners. Using `addEventListener` adds an event listener without overriding existing ones, unless they are specified with the same options. 

## How to Reproduce

1. Open `bug.html` in a web browser.
2. Click on the div element. Only the 'world' alert will be displayed.