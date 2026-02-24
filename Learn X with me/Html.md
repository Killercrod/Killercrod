In this markdown were going to talk about the basics to html and how to do basic things of frontend to make your first webpage
At first we need to understand in wich situations were going to use html, we use html when we want to make the structure of our webpage and we will do it beacuse is good practice to modulize everything that we can
| Category | Tag | Description | Example |
|----------|-----|-------------|---------|
| **Headings** | `<h1>` to `<h6>` | Headings (from most to least important) | `<h1>Main Title</h1>` |
| **Text** | `<p>` | Paragraph | `<p>This is a paragraph.</p>` |
| | `<strong>` | Strong emphasis (bold) | `<strong>Warning!</strong>` |
| | `<em>` | Emphasis (italic) | `<em>emphasis</em>` |
| | `<mark>` | Highlighted text | `<mark>important</mark>` |
| | `<small>` | Small text (legal notes, etc.) | `<small>© 2025</small>` |
| | `<br>` | Line break (void element) | `Line 1<br>Line 2` |
| | `<hr>` | Horizontal rule (void element) | `<hr>` |
| **Links & Images** | `<a>` | Hyperlink | `<a href="https://example.com">Visit</a>` |
| | `<img>` | Image (void element) | `<img src="photo.jpg" alt="Description">` |
| **Lists** | `<ul>` | Unordered list | `<ul><li>One</li><li>Two</li></ul>` |
| | `<ol>` | Ordered list | `<ol><li>First</li><li>Second</li></ol>` |
| | `<li>` | List item | (used inside `<ul>` or `<ol>`) |
| **Containers** | `<div>` | Block-level container | `<div>...</div>` |
| | `<span>` | Inline container | `<span>text</span>` |
| **HTML5 Semantics** | `<header>` | Header of a page or section | `<header><h1>Title</h1></header>` |
| | `<nav>` | Navigation menu | `<nav><a href="#">Home</a></nav>` |
| | `<main>` | Main content of the page | `<main><p>...</p></main>` |
| | `<section>` | Thematic section | `<section><h2>...</h2><p>...</p></section>` |
| | `<article>` | Independent content (post, news) | `<article><h2>Article</h2>...</article>` |
| | `<aside>` | Complementary content (sidebar) | `<aside>Advertisement</aside>` |
| | `<footer>` | Footer of a page or section | `<footer>© 2025</footer>` |
| **Tables** | `<table>` | Table container | `<table>...</table>` |
| | `<tr>` | Table row | `<tr><td>...</td></tr>` |
| | `<td>` | Table data cell | `<td>Value</td>` |
| | `<th>` | Table header cell | `<th>Name</th>` |
| | `<thead>` | Table header group | `<thead><tr>...</tr></thead>` |
| | `<tbody>` | Table body group | `<tbody>...</tbody>` |
| **Forms** | `<form>` | Form container | `<form action="/submit" method="post">...</form>` |
| | `<input>` | Input field (various types) | `<input type="text" name="username">` |
| | `<label>` | Label for a form field | `<label for="email">Email:</label>` |
| | `<textarea>` | Multi-line text area | `<textarea rows="4" cols="50"></textarea>` |
| | `<select>` | Dropdown list | `<select><option>Option 1</option></select>` |
| | `<button>` | Button | `<button type="submit">Submit</button>` |
| | `<fieldset>` | Groups related fields | `<fieldset><legend>Personal Info</legend>...</fieldset>` |
| | `<legend>` | Caption for a `<fieldset>` | `<legend>Form</legend>` |
| **Multimedia** | `<audio>` | Audio player | `<audio src="song.mp3" controls></audio>` |
| | `<video>` | Video player | `<video src="movie.mp4" controls></video>` |
| | `<iframe>` | Inline frame for embedding | `<iframe src="https://example.com"></iframe>` |
| **Others** | `<meta>` | Metadata (in `<head>`) | `<meta charset="UTF-8">` |
| | `<link>` | Links external resources | `<link rel="stylesheet" href="style.css">` |
| | `<script>` | JavaScript code | `<script src="app.js"></script>` |
| | `<style>` | Internal CSS | `<style>body {color: red;}</style>` |
This is the basic structure of html its good to know why its ordered like that

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Proyecto</title>
    <!-- Enlace al archivo CSS -->
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Bienvenido a mi proyecto</h1>
    </header>
    <main>
        <p>Este es el contenido principal.</p>
    </main>
    <footer>
        <p>&copy; 2025 Mi Proyecto</p>
    </footer>
    <!-- Enlace al archivo JavaScript (justo antes de cerrar body) -->
    <script src="js/script.js"></script>
</body>
</html>
```
I will explain why its ordered like this and why is important to know this
<!DOCTYPE html>
What is it? It's a declaration that tells the browser the document is written in HTML5 (the latest version of HTML).
Why is it necessary? Without it, the browser might interpret the page in "quirks mode" (compatibility mode with older versions), which can cause display and behavioral errors. It is the first required line in every HTML5 document.

<html lang="es">
Opening tag that wraps all the content of the page.
Attribute lang="es": indicates that the main language of the document is Spanish. This helps search engines, browsers, and screen readers interpret the content correctly (e.g., for pronunciation or suggesting translations).
Why is it necessary? It is the root of the document; without it, the browser wouldn't know it's reading HTML.

<head> ... </head>
This is the document's header; it contains metadata and information that is not directly displayed on the page (except for the title). It's like the "brain" of the page.
Everything inside <head> is mainly for the browser, search engines, and other services.

a. <meta charset="UTF-8">

Defines the character encoding for the document. UTF-8 includes practically all symbols and characters from all languages (ñ, accents, emojis, etc.).
Why is it necessary? Without this line, special characters might display incorrectly (e.g., "á" would appear as "Ã¡"). It is essential for correct text rendering.
b. <meta name="viewport" content="width=device-width, initial-scale=1.0">

Controls how the page is displayed on mobile devices. width=device-width sets the page width to the device's screen width, and initial-scale=1.0 sets the initial zoom level.
Why is it necessary? Without this tag, websites appear "zoomed out" on mobile (like a scaled-down desktop version). It's essential for responsive design.
c. <title>Mi Proyecto</title>

Defines the page title that appears in the browser tab and in search results.
Why is it necessary? It is required in HTML and improves user experience and SEO (search engine positioning).
d. <link rel="stylesheet" href="css/style.css">

Links an external CSS stylesheet.

rel="stylesheet" indicates it's a stylesheet.
href="css/style.css" is the path to the CSS file (inside the css folder).
Why is it necessary? It separates content (HTML) from presentation (CSS). It makes maintenance easier and allows styles to be reused.
<body> ... </body>
Contains all the visible content of the page: text, images, buttons, etc.
It is the body of the document.

a. <header> ... </header>

A semantic tag representing the header of the page or a section. It usually includes the logo, main title, navigation menu, etc.
Why use it? It helps with accessibility and SEO, as screen readers and search engines can easily identify the structure.
<h1>Bienvenido a mi proyecto</h1>

This is the level 1 heading, the most important one. There should be only one per page, and it describes the main topic.
Why is it necessary? It defines the content hierarchy and is key for SEO.
b. <main> ... </main>

A semantic tag that wraps the main and unique content of the page. It should not be repeated (e.g., it should not include sidebars or repeated menus).
Why use it? It improves accessibility (screen readers can jump directly to the main content) and semantic structure.
<p>Este es el contenido principal.</p>

A paragraph tag. It groups text into a block.
Why is it necessary? It defines text paragraphs, making the content readable and styleable.
c. <footer> ... </footer>

A page footer, typically containing copyright information, legal links, contact details, etc.
Why use it? For semantics and accessibility.
<p>&copy; 2025 Mi Proyecto</p>

Displays the copyright symbol © (the &copy; entity) and the year. HTML entities prevent issues with special characters.
<script src="js/script.js"></script>
Links an external JavaScript file just before closing </body>.
Why is it placed here and not in the <head>? Because scripts block HTML loading until they are downloaded and executed. By placing it at the end, we ensure the HTML content loads first, improving perceived page speed. Additionally, the script can then manipulate DOM elements that already exist.
Were going to make some basic excercises to understand better how to make some basic stuff
