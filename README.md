code-styleguide
===============

Personal styleguide and standards to develop flexible, durable and sustainable HTML and CSS.  
Current state is early alpha.  
Inspiration come from [code-guide](https://github.com/mdo/code-guide), [CSS-Guidelines](https://github.com/csswizardry/CSS-Guidelines), [Google HTML/CSS Style Guide](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml), etc.

***

# HTML

## Syntax

- Use soft-tabs with 2 spaces
- Nested elements should be indented once (2 spaces)
- Always use double quotes, never single quotes
- Don't include a trailing slash in self-closing elements

**Incorect example:**

```html
<!DOCTYPE html>
<html>
<head>
<title>Page title</title>
</head>
<body>
<img src='images/company-logo.png' alt='Company' />
<h1 class='hello-world'>Hello, world!</h1>
</body>
</html>
```

**Correct example**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page title</title>
  </head>
  <body>
    <img src="images/company-logo.png" alt="Company">
    <h1 class="hello-world">Hello, world!</h1>
  </body>
</html>
```

## Doctype

Use the most recent doctype.

## Attribute order

- `class`
- `id`, `name`
- `data-*`
- `src`, `for`, `type`, `href`
- `title`, `alt`
- `aria-*`, `role`

```html
<a class="" id="" data-modal="" href="">Example link</a>
```

## Comments

When working on big HTML files, it's a good practice to add some comments especially to know where are the closing tags.
Opening comments are one line before the opening tag. Closing comments start with a `/` and are on the same line, juste after the closing tag.
Comments follow [Emmets attribute operator](http://docs.emmet.io/abbreviations/syntax/#attribute-operators) coding style.

- `<div id="content">`: `<!-- #content -->`
- `<div class="my-class">`: `<!-- .my-class -->`
- `<form class="search">`: `<!-- .search -->`

```html
<!-- [role=main] -->
<div role="main">

  <!-- .row -->
  <div class="row">
    <!-- .pull-right -->
    <figure class="pull-right"-->
      ...
    </figure><!-- /.pull-right -->
  </div><!-- /.row -->

<!-- /[role=main] -->
```

## JavaScript generated markup

Writing markup in a javascript file makes the content harder to find, harder to edit, and less performant. Don't do it.

# CSS

## Syntax

- Use soft-tabs with two spaces
- When grouping selectors, keep individual selectors to a single line
- Include one space before the opening brace of declaration blocks
- Place closing braces of declaration blocks on a new line
- Include one space after `:` in each property
- Each declaration should appear on its own line
- End all declarations with a semi-colon
- Comma-separated values should include a space after each comma
- Don't include spaces after commas in RGB or RGBa colors, and don't preface values with a leading zero
- Lowercase all hex values, e.g., `#fff` instead of `#FFF`
- Use shorthand hex values where available, e.g., `#fff` instead of `#ffffff`
- Quote attribute values in selectors, e.g., `input[type="text"]`
- Avoid specifying units for zero values, e.g., `margin: 0;` instead of `margin: 0px;`

**Incorrect example:**

```css
.selector, .selector-secondary, .selector[type=text] {
  padding:15px;
  margin:0px 0px 15px;
  background-color:rgba(0, 0, 0, 0.5);
  box-shadow:0 1px 2px #CCC,inset 0 1px 0 #FFFFFF
}
```

**Correct example:**

```css
.selector,
.selector-secondary,
.selector[type="text"] {
  padding: 15px;
  margin: 0 0 15px;
  background-color: rgba(0,0,0,.5);
  box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #fff;
}
```
