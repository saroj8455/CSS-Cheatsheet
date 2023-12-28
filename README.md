# css-cheatsheet

A complete CSS cheat sheet for developers.

## Browse to find the images that fit your needs and click to download. Use the on-the-fly color image generation to match your brand identity.

`https://undraw.co/illustrations`
`https://www.manypixels.co/gallery`

### Selector:

```css
/* Element Selector */
p {
  /* Styles */
}

/* Class Selector */
.myClass {
  /* Styles */
}

/* ID Selector */
#myId {
  /* Styles */
}

/* Attribute Selector */
input[type='text'] {
  /* Styles */
}

/* Descendant Selector */
div p {
  /* Styles */
}

/* Pseudo-class Selector */
a:hover {
  /* Styles */
}
```

### Typography:

```css
/* Font Family */
.element {
  font-family: Arial, sans-serif;
}

/* Font Size */
.element {
  font-size: 16px;
}

/* Font Weight */
.element {
  font-weight: bold;
}

/* Text Color */
.element {
  color: #333;
}

/* Text Alignment */
.element {
  text-align: center;
}
```

### Display and Positioning:

```css
/* Display */
.element {
  display: block;
}

/* Position */
.element {
  position: relative;
}

/* Flexbox */
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Grid */
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
```

### Background and Borders:

```css
/* Background Color */
.element {
  background-color: #f0f0f0;
}

/* Background Image */
.element {
  background-image: url('path/to/image.jpg');
}

/* Border Radius */
.element {
  border-radius: 5px;
}

/* Box Shadow */
.element {
  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
}
```

### Animations and Transitions:

```css
/* Transition */
.element {
  transition: all 0.3s ease-in-out;
}

/* Keyframes Animation */
@keyframes slide {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(100px);
  }
}

.element {
  animation: slide 2s infinite alternate;
}
```

### CSS Rest and Basic Rules

```css
/* This rule resets the margin and padding of all elements on the page to 0. It also sets the `box-sizing` property to `border-box`, which means that the width and height of an element will include its border.  */
/* Resetting Margins and Padding */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* This rule sets the default text color for the page to a dark gray color. It also sets the `--primary-text-color` variable to a blue color. This variable can be used to change the color of text throughout the page. */
:root {
  --text-color: #37415a;
  --primary-text-color: #0b49e7;
}

/* Setting the Default Font Family and Font Size */
html,
body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
    Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  font-size: 1.2rem;
  line-height: 1.6;
  color: var(--primary-text-color);
}
```

### CSS tips for working inconstinstenently sized logos

If you have a logo that is not a consistent size across different devices or screen sizes, it can be tricky to make sure it scales properly without <br>

```html
<section>
  <div class="container">
    <div class="photos">
      <img src="./assets/adidas.png" alt="adidas" srcset="" />
      <img src="./assets/nba.png" alt="nba" srcset="" />
      <img src="./assets/nike.png" alt="nike" srcset="" />
      <img src="./assets/puma.png" alt="puma" srcset="" />
      <img src="./assets/rebook.png" alt="rebook" srcset="" />
    </div>
  </div>
</section>
```

```css
/* Create a container  margin-inline: auto; define same margin both left and right */
.container {
  max-width: 90%;
  margin-inline: auto;
}

/* Reset default rule of image */
img {
  max-width: 100%;
  max-height: 100%;
  display: block;
}

.image-container {
  background-color: var(--bg-primary);
  height: 100dvh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.photos {
  padding: 2rem;
  display: flex;
  align-items: center;
  gap: 2rem;
}

.photos img {
  width: 15%;
  /* Make the images same size */
  aspect-ratio: 3/2;
  object-fit: contain;
  /* Reset the white background */
  mix-blend-mode: color-burn;
}
```

##### Output :

![Alt text](image.png)

### Avoid media query

`https://undraw.co/illustrations` <br>

```css
// simple reset
*,
*::before,
*::after {
  box-sizing: border-box;
}

* {
  margin: 0;
  padding: 0;
  font: inherit;
}

// base styles

body {
  font-size: $fs-400;
  font-weight: $fw-400;
  color: $color-neutral-900;
  background-color: $color-neutral-100;
  font-family: $ff-sans;
  text-align: center;
}

.container {
  width: min(100% - 2rem, 60rem);
  margin-inline: auto;
}
```

### Define variable in css

```css
:root {
  --clr-primary-400: 263 55% 52%;
  --clr-secondary-400: 217 19% 35%;
  --clr-secondary-500: 219 29% 14%;
  --clr-neutral-100: 0 0% 100%;
  --clr-neutral-200: 210 46% 95%;
  --clr-neutral-300: 0 0% 81%;

  --ff-primary: 'Barlow Semi Condensed', sans-serif;

  --fw-400: 500;
  --fw-700: 600;

  --fs-300: 0.6875rem;
  --fs-400: 0.8125rem;
  --fs-500: 1.25rem;
}
```

### Default reset style

```css
/* Box sizing rules */
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* Remove list styles on ul, ol elements with a list role, which suggests default styling will be removed */
ul[role='list'],
ol[role='list'] {
  list-style: none;
}
/* Set core root defaults */
html:focus-within {
  scroll-behavior: smooth;
}
/* Set core body defaults */
body {
  min-height: 100vh;
  text-rendering: optimizeSpeed;
  line-height: 1.5;
}
/* A elements that don't have a class get default styles */
a:not([class]) {
  text-decoration-skip-ink: auto;
}

/* Make images easier to work with */
img,
picture {
  max-width: 100%;
  display: block;
}
/* Inherit fonts for inputs and buttons */
input,
button,
textarea,
select {
  font: inherit;
}
```

### Free resource repo

`https://box-shadow.dev/` <br>
`https://github.com/bradtraversy/design-resources-for-developers.git` <br>
`https://github.com/bradtraversy/traversy-js-challenges` <br>

### Remove default margin for html element <Kevin Powell>

`https://github.com/kevin-powell/learn-grid-the-easy-way/blob/main/style.css` <br>

```css
/* Remove default margin */
body,
h1,
h2,
h3,
h4,
p,
figure,
blockquote,
dl,
dd {
  margin: 0;
}
```

### VerifyToken

```js
const jwt = require('jsonwebtoken');
const asyncHandler = require('express-async-handler');
const User = require('../models/userModel');

const protect = asyncHandler(async (req, res, next) => {
  let token;

  if (
    req.headers.authorization &&
    req.headers.authorization.startsWith('Bearer')
  ) {
    try {
      // Get token from header
      token = req.headers.authorization.split(' ')[1];

      // Verify token
      const decoded = jwt.verify(token, process.env.JWT_SECRET);

      // Get user from the token
      req.user = await User.findById(decoded.id).select('-password');

      next();
    } catch (error) {
      console.log(error);
      res.status(401);
      throw new Error('Not authorized');
    }
  }

  if (!token) {
    res.status(401);
    throw new Error('Not authorized, no token');
  }
});

module.exports = { protect };
```

### Common CSS Style author : Brad Traversy

```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  height: 100vh;
}

a {
  text-decoration: none;
  color: #000;
}

p {
  line-height: 1.7;
}

ul {
  list-style: none;
}

li {
  line-height: 2.2;
}

h1,
h2,
h3 {
  font-weight: 600;
  margin-bottom: 10px;
}

.container {
  width: 100%;
  max-width: 960px;
  margin: 0 auto;
  padding: 0 20px;
  text-align: center;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
  border-bottom: 1px solid #e6e6e6;
  margin-bottom: 60px;
}

.header ul {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header ul li {
  margin-left: 20px;
}

.header ul li a {
  display: flex;
  align-items: center;
}

.header ul li a:hover {
  color: #777;
}

.header ul li a svg {
  margin-right: 5px;
}

.heading {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 50px;
  padding: 0 20px;
}

.heading p {
  color: #828282;
}

.goals {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
}

.goal {
  background-color: #f4f4f4;
  margin: 10px 0;
  padding: 20px 0 10px;
  position: relative;
}

.goal .close {
  position: absolute;
  top: 10px;
  right: 15px;
  cursor: pointer;
  border: none;
  background: none;
}

.form,
.content {
  width: 70%;
  margin: 0 auto;
}

.form-group {
  margin-bottom: 10px;
}

.form-group input,
.form-group textarea,
.form-group select {
  width: 100%;
  padding: 10px;
  border: 1px solid #e6e6e6;
  border-radius: 5px;
  margin-bottom: 10px;
  font-family: inherit;
}

.form-group label {
  text-align: left;
  display: block;
  margin: 0 0 5px 3px;
}

.btn {
  padding: 10px 20px;
  border: 1px solid #000;
  border-radius: 5px;
  background: #000;
  color: #fff;
  font-size: 16px;
  font-weight: 700;
  cursor: pointer;
  text-align: center;
  appearance: button;
  display: flex;
  align-items: center;
  justify-content: center;
}

.btn svg {
  margin-right: 8px;
}

.btn-reverse {
  background: #fff;
  color: #000;
}

.btn-block {
  width: 100%;
  margin-bottom: 20px;
}

.btn:hover {
  transform: scale(0.98);
}

.loadingSpinnerContainer {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 5000;
  display: flex;
  justify-content: center;
  align-items: center;
}

.loadingSpinner {
  width: 64px;
  height: 64px;
  border: 8px solid;
  border-color: #000 transparent #555 transparent;
  border-radius: 50%;
  animation: spin 1.2s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

@media (max-width: 600px) {
  .form {
    width: 90%;
  }

  .heading h1 {
    font-size: 2rem;
  }

  .heading p {
    font-size: 1.5rem;
  }
}
```

### CSS Must know property @author Lukas | Web Devlopment and Design

`https://getcssscan.com/css-box-shadow-examples` <br>
