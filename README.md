# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1 - Braily

What are the main differences between Flexbox and Grid layouts? Describe scenarios where each layout system would be more suitable.

### Response 1

The main difference between **Flexbox** and Grid layouts is that **Flexbox** was designed for layout in one dimension, either a row or a column. **Grid** was designed for a two-dimensional layout, with rows and columns, at the same time.

- A scenario where you would want to use **Flexbox** is when trying to arrange items in a single dimension, like a row or a column. This would be used for simpler layouts like navigation bars or simply aligning items on a container.

- A scenario where you would want to use **Grid** is when you're looking for a complex two-dimensional layout where you need control of your rows and columns simultaneously

## Prompt 2

What is the difference between `justify-content` and `align-items` in Flexbox? How does each property control the positioning of flex items within the container?

### Response 2

## Prompt 3 - Braily

Describe the difference between `grid-template-areas` and `grid-template-columns`/`grid-template-rows`. When might you prefer one approach over the other?

### Response 3

`grid-template-columns` and `grid-template-rows` are used to define the size and structure of the grid. They specify the number and dimensions of columns and rows in the grid.

For example:

```css
grid-template-columns: 60px 80px;
```

- This defines a grid with two columns: the first column is 60 pixels wide, and the second column is 80 pixels wide.

```css
grid-template-rows: 1fr 2fr 1fr;
```

- This defines three rows: the first row takes 1 fraction of the available space, the second takes 2 fractions, and the third takes 1 fraction.

`grid-template-areas` provides a way to assign names to grid areas and visually map out your layout using text-based representations. This approach makes it easier to manage layouts where elements need to span multiple rows or columns.

For example:

```css
grid-template-areas: 
  "header header header"
  "sidebar content content"
  "footer footer footer";
```

- This layout defines three rows:
  - The first row has a single "header" area spanning three columns.
  - The second row includes a "sidebar" area and a "content" area spanning two columns.
  - The third row has a "footer" area spanning all three columns.

#### When to prefer one approach over the other
- Use `grid-template-columns`/`grid-template-rows` when you need precise control over grid sizing without explicitly naming areas. This approach is ideal for simpler layouts where the structure doesn't need to be referenced semantically or rearranged frequently.
- Use `grid-template-areas` when you want a clear, semantic representation of your layout. This approach is especially helpful for larger, more complex grids, as it improves readability and maintainability. It also makes it easier to rearrange or update the layout, as the named areas can be referenced directly in your CSS.

## Prompt 4

Explain the `min-width` and `max-width` keywords in media queries. How do they help create responsive breakpoints for different screen sizes?

### Response 4

## Prompt 5

Imagine you are teaching a brief lesson on **mobile first design**. Your lesson should include the following information:

* An explanation of mobile first design and a few of the benefits of this approach
* A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
* An explanation of the code example.

### Response 5

