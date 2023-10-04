# Secret Message Sharing App

## Overview

This project is a simple web application that allows users to create a secret message, encrypt it, and share it with others via a link. The app uses the [Materialize CSS](https://materializecss.com/) library for a clean and simple design.

![App Screenshot](/path-to-your-screenshot.png)

## Technology Used 

- HTML5
- CSS3 (Using Materialize CSS from CDN)
- JavaScript (Client-Side)

## How It Works 

- The user inputs a secret message into the provided text box.
- Upon clicking "Create", the message is encrypted using JavaScript’s `btoa()` function and appended to the URL fragment.
- The encrypted URL can be shared. When the recipient opens the link, the app decrypts the message using `atob()` and displays it.

## Main Code

### index.html 

The HTML uses Materialize CSS for styling and basic structure. There are three main parts in the `body`:

1. A `div` to display the decrypted message (`message-show`).
2. A form to allow the user to input a message (`message-form`).
3. A `div` to display the generated URL for sharing (`link-form`).

### index.js 

The JavaScript handles the encryption/decryption logic and DOM manipulation to show/hide elements as necessary.

```javascript
const { hash } = window.location;
const message = atob(hash.replace('#', ''));
...
