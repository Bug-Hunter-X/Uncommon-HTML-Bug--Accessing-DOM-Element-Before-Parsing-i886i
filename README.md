# Uncommon HTML Bug: DOM Access Before Parsing

This repository demonstrates an uncommon bug in HTML related to accessing elements in the DOM before the browser has fully parsed the HTML.

The `bug.html` file contains the erroneous code.  The `bugSolution.html` file shows the corrected code.

## Bug Description:

Attempting to manipulate a DOM element (specifically, setting its `display` style to `none`) using JavaScript *before* the browser has finished parsing that element's HTML can lead to unexpected behavior, including the element not being hidden as expected. This often happens because the element might not be present in the DOM when the JavaScript is executed.

## Solution:

The solution involves ensuring the DOM element is fully parsed before attempting to access or manipulate it.  This is commonly achieved using the `DOMContentLoaded` event listener.