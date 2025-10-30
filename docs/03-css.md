# Introduction to CSS

## What is CSS?

CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a document written in HTML or XML. CSS defines how elements should be rendered on screen, on paper, in speech, or on other media.

## Benefits of CSS

- **Separation of Content and Design:** CSS separates the structure of a webpage (HTML) from its presentation (CSS). This makes maintenance easier and allows for changes in design without altering the content.
- **Reusability:** CSS allows the reuse of styles across multiple pages, ensuring consistency and reducing redundancy.
- **Improved Performance:** CSS enhances webpage load times by allowing the browser to cache stylesheets, leading to faster page loads.
- **Flexibility and Control:** CSS provides greater control over the layout and design, enabling complex and responsive designs.

## Basic CSS Syntax

CSS is composed of selectors and declarations. A selector targets HTML elements, and declarations define the styles to be applied to those elements.

### Example

```css
selector {
  property: value;
}
```

### Explanation

- **Selector:** The HTML element(s) to be styled.
- **Property:** The CSS property to be applied (e.g., color, font-size).
- **Value:** The value of the property (e.g., red, 16px).

## Common CSS Properties

### Colors

- `color`: Sets the color of text.
- `background-color`: Sets the background color of an element.

### Text

- `font-family`: Sets the font of the text.
- `font-size`: Sets the size of the text.
- `text-align`: Aligns text (left, right, center, justify).

### Box Model

- `margin`: Sets the space outside the border of an element.
- `border`: Sets the border around an element.
- `padding`: Sets the space inside the border, around the content.
- `width`: Sets the width of an element.
- `height`: Sets the height of an element.

### Display and Position

- `display`: Sets the display behavior of an element (e.g., block, inline, none).
- `position`: Sets the positioning method of an element (e.g., static, relative, absolute, fixed).
- `top`, `right`, `bottom`, `left`: Sets the position of an element.

### Flexbox

- `display: flex`: Enables flexbox layout for a container.
- `flex-direction`: Sets the direction of the flex items.
- `justify-content`: Aligns flex items along the main axis.
- `align-items`: Aligns flex items along the cross axis.

## Example CSS

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Basic HTML Tags with CSS</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        line-height: 1.6;
        margin: 0;
        padding: 0;
      }
      header {
        background: #333;
        color: #fff;
        padding: 1rem;
        text-align: center;
      }
      nav ul {
        list-style: none;
        padding: 0;
      }
      nav ul li {
        display: inline;
        margin-right: 10px;
      }
      nav ul li a {
        color: #fff;
        text-decoration: none;
      }
      main {
        padding: 20px;
      }
      section {
        margin-bottom: 20px;
      }
      h1,
      h2,
      h3 {
        color: #333;
      }
      ul,
      ol,
      dl {
        margin: 10px 0;
      }
      p {
        margin: 10px 0;
      }
      pre {
        background: #f4f4f4;
        padding: 10px;
        overflow: auto;
      }
      blockquote {
        border-left: 10px solid #ccc;
        margin: 10px 0;
        padding-left: 10px;
        color: #666;
      }
      form {
        background: #f9f9f9;
        padding: 20px;
        border: 1px solid #ddd;
      }
      form label {
        display: block;
        margin-bottom: 5px;
      }
      form input,
      form select,
      form textarea {
        width: 100%;
        padding: 8px;
        margin-bottom: 10px;
        border: 1px solid #ccc;
        border-radius: 4px;
      }
      form input[type="submit"] {
        width: auto;
        background: #333;
        color: #fff;
        border: none;
        cursor: pointer;
      }
      footer {
        background: #333;
        color: #fff;
        text-align: center;
        padding: 10px 0;
        position: fixed;
        width: 100%;
        bottom: 0;
      }
    </style>
  </head>
  <body>
    <header>
      <h1>Welcome to the Basic HTML Tags Page</h1>
      <nav>
        <ul>
          <li><a href="#section1">Section 1</a></li>
          <li><a href="#section2">Section 2</a></li>
          <li><a href="#section3">Section 3</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <section id="section1">
        <h2>Section 1: Text Elements</h2>
        <p>
          This is a paragraph with some <strong>bold</strong> text and some
          <em>italic</em> text.
        </p>
        <blockquote>This is a blockquote.</blockquote>
        <pre>
                This is preformatted text.
            </pre
        >
        <p>
          This is a <a href="https://www.example.com" target="_blank">link</a>.
        </p>
      </section>

      <section id="section2">
        <h2>Section 2: Lists</h2>
        <h3>Unordered List</h3>
        <ul>
          <li>Item 1</li>
          <li>Item 2</li>
          <li>Item 3</li>
        </ul>

        <h3>Ordered List</h3>
        <ol>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item</li>
        </ol>

        <h3>Definition List</h3>
        <dl>
          <dt>Term 1</dt>
          <dd>Definition 1</dd>
          <dt>Term 2</dt>
          <dd>Definition 2</dd>
        </dl>
      </section>

      <section id="section3">
        <h2>Section 3: Media and Forms</h2>
        <h3>Image</h3>
        <img src="https://via.placeholder.com/150" alt="Placeholder Image" />

        <h3>Form</h3>
        <form action="/submit" method="post">
          <label for="name">Name:</label>
          <input type="text" id="name" name="name" /><br /><br />

          <label for="email">Email:</label>
          <input type="email" id="email" name="email" /><br /><br />

          <label for="password">Password:</label>
          <input type="password" id="password" name="password" /><br /><br />

          <label for="date">Date:</label>
          <input type="date" id="date" name="date" /><br /><br />

          <label for="gender">Gender:</label>
          <select id="gender" name="gender">
            <option value="male">Male</option>
            <option value="female">Female</option></select
          ><br /><br />

          <label for="comments">Comments:</label><br />
          <textarea id="comments" name="comments" rows="4" cols="50"></textarea
          ><br /><br />

          <label for="subscribe">Subscribe to newsletter:</label>
          <input type="checkbox" id="subscribe" name="subscribe" /><br /><br />

          <input type="submit" value="Submit" />
        </form>
      </section>
    </main>

    <footer>
      <p>© 2024 Basic HTML Tags Page</p>
    </footer>
  </body>
</html>
```

- `font-family`: Specifies the font for text.
- `line-height`: Sets the amount of space between lines of text.
- `margin`: Defines space around elements; can be individual (top, right, bottom, left) or combined.
- `padding`: Defines space inside elements, between the content and border.
- `background`: Sets the background color of an element.
- `color`: Sets the color of text.
- `text-align`: Aligns text horizontally within an element.
- `list-style`: Removes bullet points from list items.
- `display`: Specifies how an element is displayed; `inline` makes elements sit next to each other.
- `margin-right`: Sets space to the right of an element.
- `text-decoration`: Adds or removes decorations to text, such as underlines.
- `padding`: Adds space inside elements.
- `overflow`: Manages content overflow, such as adding scroll-bars.
- `border`: Adds a border around elements.
- `border-left`: Adds a border on the left side of an element.
- `padding-left`: Adds space to the left inside an element.
- `background`: Defines the background color of an element.
- `display`: Sets elements as block, meaning they take up the full width available.
- `width`: Sets the width of an element.
- `padding`: Adds padding inside an element.
- `margin-bottom`: Adds space below an element.
- `border-radius`: Rounds the corners of an element.
- `cursor`: Changes the mouse cursor when it hovers over an element.
- `position`: Sets the positioning method used for an element.
- `bottom`: Sets the bottom edge of an element.

---

[Table of Contents](00-Cover.md#table-of-contents)
