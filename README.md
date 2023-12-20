# css-cheatsheet
A complete CSS cheat sheet for developers.


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
input[type="text"] {
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

