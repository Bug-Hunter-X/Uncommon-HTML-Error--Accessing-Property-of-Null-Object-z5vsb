# Uncommon HTML Error: Accessing Property of Null Object

This repository demonstrates a subtle error that can occur in HTML/JavaScript code when attempting to manipulate DOM elements before ensuring their existence.  The bug occurs when trying to access a property of an element that hasn't been found or might not exist.

## Bug Description:

The provided `bug.html` file contains a script that attempts to assign a value to a non-existent property of a DOM element.  The problem is that the script doesn't first verify if the element actually exists using `getElementById` before attempting to access the property. This leads to a JavaScript error in the browser's console.

## Solution:

The `bugSolution.html` file demonstrates the correct approach.  Before assigning the property, it checks if the element exists using `getElementById`.  If the element is found (not null), then the property is assigned; otherwise, a more graceful handling of the situation is shown by logging a message to the console indicating the element wasn't found.