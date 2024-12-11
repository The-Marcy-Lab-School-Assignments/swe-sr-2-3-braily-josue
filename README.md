# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

What are the main differences between Flexbox and Grid layouts? Describe scenarios where each layout system would be more suitable.

### Response 1

## Prompt 2 - Josue

What is the difference between `justify-content` and `align-items` in Flexbox? How does each property control the positioning of flex items within the container?

### Response 2

In Flexbox, there are two key properties used to position items within a container: `justify-content` and `align-items`. These properties control how flex items are spaced and aligned along two different axes. Containers are any HTML element that holds items to manipulate the flexbox layout system, e.g., `<div>, <section>, <article>`, etc.

---

The Two Axes in Flexbox

- Main Axis: This is the default direction of the flex container, which is horizontal by default (left to right).  
  The `justify-content` property works along this axis.
- Cross Axis: This is the direction perpendicular to the main axis (top to bottom).  
  The `align-items` property works along this axis.

---

What Does `justify-content` Do?

`justify-content` controls how flex items are arranged along the main axis. Think of it as spacing the items left to right (or top to bottom, if the container's direction is vertical).

Common Values:

- `flex-start`: Items align at the start of the main axis.
- `center`: Items align in the center of the main axis.
- `flex-end`: Items align at the end of the main axis.
- `space-between`: Items are spaced evenly, with the first item at the start and the last at the end.
- `space-around`: Items are spaced evenly, with equal space around them.
- `stretch` (default): Items stretch to fill the container along the cross axis.

---

What Does `align-items` Do?

`align-items` controls how flex items are arranged along the cross axis. Think of it as positioning items up and down (or left to right, if the container's direction is vertical).

---

### HTML Code Example

```html
<div class="container">
  <!-- The container. (Containers are any HTML element that holds items to manipulate the flexbox layout system, e.g., <div>, <section>, <article>, etc.) -->
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```

```css
.container {
  display: flex;
  justify-content: center; /* Centers items left-to-right */
  align-items: center; /* Centers items up-and-down */
  height: 200px; /* So we can see vertical alignment */
  border: 1px solid black;
}

.item {
  width: 50px;
  height: 50px;
  background-color: lightblue;
  margin: 5px;
}
```

---

## Prompt 3

Describe the difference between `grid-template-areas` and `grid-template-columns`/`grid-template-rows`. When might you prefer one approach over the other?

### Response 3

---

## Prompt 4 - Josue

Explain the `min-width` and `max-width` keywords in media queries. How do they help create responsive breakpoints for different screen sizes?

### Response 4

`min-width` and `max-width` are like rules you set for your website’s design to make it look good on different screen sizes. `min-width` means "start using these styles when the screen is at least this wide." It’s great for building mobile-first designs, where you add more styles as the screen gets bigger. `max-width` means "use these styles only if the screen is this wide or smaller." It’s often used when designing for bigger screens first and adjusting for smaller ones. Together, they let you create breakpoints—those are the spots where your design changes to fit better, like making things stack on a phone or spread out on a big monitor.

---

## Prompt 5 - Josue

Imagine you are teaching a brief lesson on **mobile-first design**. Your lesson should include the following information:

- An explanation of mobile-first design and a few of the benefits of this approach.
- A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
- An explanation of the code example.

### Response 5

Mobile-First Design is a way of designing websites where you start with the smallest screen sizes (like phones) and then add more styles for larger screens (like tablets and desktops). The idea is to focus on the essentials first, ensuring the site works well on mobile, and then enhance it as the screen size grows.

Benefits of Mobile-First Design:

- Ensures your site works well on mobile, where most users are.
- Loads faster because it starts with simpler styles.
- Easier to scale up than scale down.

CSS Example (Using Flexbox):  
Here’s how you can make a container adjust from stacking items on mobile to arranging them in a row on larger screens:

```css
/* Base styles for mobile */
.container {
  display: flex;
  flex-direction: column; /* Stacks items vertically */
  gap: 10px; /* Adds space between items */
}

/* Tablet and larger */
@media (min-width: 768px) {
  .container {
    flex-direction: row; /* Aligns items in a row */
    justify-content: space-between; /* Spreads them out */
  }
}
```
