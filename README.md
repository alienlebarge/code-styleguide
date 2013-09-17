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

1. `class`
1. `id`
1. `data-*`
1. `for` /  `type` /  `href`

```html
<a class="" id="" data-modal="" href="">Example link</a>
```


