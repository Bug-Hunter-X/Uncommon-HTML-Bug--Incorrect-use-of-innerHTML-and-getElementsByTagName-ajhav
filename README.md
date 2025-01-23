# Uncommon HTML Bug: Incorrect use of innerHTML and getElementsByTagName

This repository demonstrates an uncommon bug related to the use of `innerHTML` and `getElementsByTagName` in JavaScript within an HTML context.  The bug highlights potential issues when manipulating the DOM and demonstrates a more robust approach to avoid these problems.

## Bug Description

The original code attempts to modify the content and style of an HTML element using `innerHTML` and `getElementsByTagName`. However, this approach contains errors:

1. Using `innerHTML` directly can lead to unexpected behavior if the modified content contains event handlers or other dynamic elements.  Modifying only specific portions of innerHTML is a better approach.
2. Using `forEach` directly on the `HTMLCollection` returned by `getElementsByTagName` will fail. `HTMLCollection` is not an array; therefore it does not have a `forEach` method. Instead convert it to an array first.

## Solution

The solution demonstrates a more robust method for updating the DOM using `textContent` and array conversion, which will avoid such problems.