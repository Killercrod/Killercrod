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

Were going to make some basic excercises to understand better how to make some basic stuff
