# :focus-visible Pseudo-class Inconsistency with Programmatic Focus

This repository demonstrates a problem with the CSS `:focus-visible` pseudo-class where the styling is applied even when focus is programmatically set, bypassing the intended user-initiated focus behavior.  This is particularly noticeable with assistive technologies.

## Issue

The `:focus-visible` pseudo-class aims to improve accessibility by applying focus styles only when the focus is initiated by the user (keyboard or mouse). In this example, when focus is set using JavaScript, the `:focus-visible` style is still applied, which contradicts its intended function.  This may lead to visual clutter and confusion for users.

## Reproduction Steps

1. Clone the repository.
2. Open `index.html` in your web browser.
3. Observe the behavior of the button when focused using the mouse/keyboard versus when focused programmatically via the JavaScript event listener.

## Solution

The solution might involve a more nuanced approach to JavaScript focus management, potentially using an event listener on the element to detect if it's focused after a user action. But the core issue still lies in inconsistent support across browsers.  Comprehensive testing is needed to ensure consistent behavior across different browsers and assistive technologies.