# HTML Basics

HTML (HyperText Markup Language) is the standard language for creating web pages. It uses elements to structure content. Each element consists of a start tag, content, and an end tag.

## Basic HTML Tags

### `<html>`

The root element of an HTML document.

### `<head>`

Contains metadata and links to resources such as stylesheets and scripts.

### `<title>`

Sets the title of the web page, displayed in the browser tab.

### `<body>`

Contains the content of the HTML document, including text, images, links, and other elements.

### `<h1>` to `<h6>`

Defines HTML headings. `<h1>` is the highest (or most important) level, and `<h6>` is the lowest.

### `<p>`

Defines a paragraph of text.

### `<a>`

Defines a hyperlink, which is used to link from one page to another.

### `<img>`

Embeds an image into the web page.

### `<ul>`, `<ol>`, `<li>`

Defines lists. `<ul>` for unordered (bulleted) lists, `<ol>` for ordered (numbered) lists, and `<li>` for list items.

### `<table>`, `<tr>`, `<td>`, `<th>`

Defines tables. `<table>` for the table itself, `<tr>` for table rows, `<td>` for table data cells, and `<th>` for table headers.

### `<div>`

Defines a division or section in an HTML document, often used as a container for other elements.

### `<span>`

Used to group inline elements and apply styles or scripts to them.

### `<form>`, `<input>`, `<label>`, `<button>`

Defines a form for user input. `<form>` is the form element, `<input>` is used to create input fields, `<label>` is used to define labels for inputs, and `<button>` creates a clickable button.

## Example HTML Page Using All Tags

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Basic HTML Tags</title>
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

- `<!DOCTYPE html>`: Defines the document type and version of HTML.
- `<html>`: The root element of an HTML document.
- `<head>`: Contains metadata and links to external resources like stylesheets.
- `<meta>`: Defines metadata such as character set and viewport settings.
- `<title>`: Specifies the title of the web page, shown in the browser tab.
- `<body>`: Contains the content of the HTML document, visible to users.
- `<header>`: Represents introductory content or a set of navigational links.
- `<h1>` to `<h3>`: Heading tags, used to define headings of different levels.
- `<nav>`: Defines a section with navigation links.
- `<ul>`: Creates an unordered (bulleted) list.
- `<ol>`: Creates an ordered (numbered) list.
- `<li>`: Defines a list item within `<ul>` or `<ol>`.
- `<dl>`: Defines a definition list.
- `<dt>`: Defines a term/name in a definition list.
- `<dd>`: Describes a term/name in a definition list.
- `<p>`: Represents a paragraph of text.
- `<strong>`: Indicates that text is of strong importance, usually rendered in bold.
- `<em>`: Indicates emphasized text, usually rendered in italics.
- `<blockquote>`: Defines a section quoted from another source.
- `<pre>`: Represents preformatted text, preserving whitespace and line breaks.
- `<a>`: Defines a hyperlink to another document or resource.
- `<section>`: Defines a section in the document, typically with its own heading.
- `<img>`: Embeds an image in the document.
- `<form>`: Defines an HTML form for user input.
- `<label>`: Defines a label for an input element.
- `<input>`: Defines an input control.
- `<textarea>`: Defines a multiline text input control.
- `<select>`: Creates a drop-down list.
- `<option>`: Defines an option in a drop-down list.
- `<footer>`: Represents the footer of a document or section, typically containing information about the author, copyright, and related links.

---

[Table of Contents](00-Cover.md#table-of-contents)
