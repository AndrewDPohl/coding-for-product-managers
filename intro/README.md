# <img src="https://cloud.githubusercontent.com/assets/8397980/19818474/bd21af4c-9d04-11e6-8df6-1ed154718dce.png" height="60">

# Hello World!

### Introductions
* Why are you here?
* [What are we going to build?](p-school-blog.herokuapp.com)

### Initial Setup
* [Cloud9](c9.io)
* [Github](github.com)

### IDE/CLI
* Create our first workspace in Cloud9
    * HTML5
    * GUI
    * IDE
    * CLI
* Shell Commands ([POSIX](http://pubs.opengroup.org/onlinepubs/9699919799/)/[UNIX](https://upload.wikimedia.org/wikipedia/commons/c/cd/Unix_timeline.en.svg))
    * `ls` (`-t`, `-a`)
    * `pwd`
    * `man`
    * `mkdir`
    * `cd`
    * `touch`
    * `mv`
    * `rm`

*> Exercise: follow along with me to learn some command line basics*

### HTML

Hyper-text Markup Language represents the frame or skeleton of any web page that you see on the Internet. Any front-end or full-stack developer will be working with it daily. The basic concepts of HTML can be learned quickly and you’ll have time to deepen your knowledge of specific attributes, tricks, and tools over time.

#### HTML page structure, head & body

Let's create an index HTML file: `$ touch index.html`

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    Content Here
  </body>
</html>
```
HTML body tags (full list: https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

Commonly Used Tags:

- Headings: `<h1> - <h6> <h1>Hello World</h1>`
- Span: `<span>Copy text </span>`
- **Div**: `<div> [content to be placed inside] </div>`
  - inspect FB page with Chrome Dev Tools

*> Exercise: Change the title. Then add a heading of whatever size you want within the body and put one of the words into a span*

Let's create a page directory: `$ mkdir pages`

#### Lists:

- Unordered list: `<ul> [list items] </ul>`
- List item: `<li> item </li>`

Let's create a menu file: `$ touch pages/products.html`

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Products</title>
  </head>
  <body>
    <ul>
      <li>Burrito</li>
      <li>Dumplings</li>
      <li>Spaghetti</li>
    </ul>
  </body>
</html>
```
*Exercise: add another product to the list*


#### Form:

- Label `<label>`
- Input `<input>`
- Horizontal Rule (aka: horizontal divider line): `<hr>`
- Line break: `<br>`

Let's create a contact us file: `$ touch pages/contact_us.html`

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Contact Us</title>
  </head>
  <body>
    <form>
      <div>
        <label>Email</label> <input required="required" type="email"/>
      </div>
      <div>
        <label>Image</label> <input required="false" type="file"/>
      </div>
      <div>
        <label>Compress Photo?</label>
        <input type="checkbox" value="1"/>
      </div>
      <br>
      <div>
        <label>Category</label>
        <select>
          <option value="1">Compliment</option>
          <option value="2">Complaint</option>
          <option value="3">General Inquiry</option>
        </select>
      </div>
      <hr>
      <div>
        <input type="submit" value="Submit"/>
      </div>
    </form>
  </body>
</html>
```
*Exercise: add another dropdown menu item and another horizontal rule*

- Common form text field types: text, email, password, search, URL
- Built-in validators
- Form field types without text field ‘input’: checkbox, file, radio, number range
- Form buttons: button, reset, submit

#### Image:

- Image: `<img src=”file-path-or-URL” alt=”alternative title”/>`

Let's create an about file: `$ touch pages/about.html`

```html
<!DOCTYPE html>
<html>
  <head>
    <title>About</title>
  </head>
  <body>
    <div class="image_container">
      <img src="https://imgs.xkcd.com/comics/code_quality_2.png"/>
    </div>
  </body>
</html>
```

*Exercise: add an image of your choosing*


#### Navigation:

- Nav: `<nav> [nav items in here] </nav>`
- Links: `<a href="URL">Link title</a>`

```html
<nav>
  <a href="index.html">Home</a> |
  <a href="pages/about.html">About</a> |
  <a href="pages/products.html">Products</a> |
  <a href="pages/contact_us.html">Contact Us</a>
</nav>
```
*Exercise: add this to each page at the top of the body and test it out. Something is broken - why?*

# CSS Part 1

Cascading Style Sheets tell the browser how to display HTML elements. CSS is quite nuanced but extremely powerful.

#### In-line Styling
`<tag style=”attribute: value;”>content</tag>`

*Exercise: add a `color` and `font-family` to the heading on your home page*

## Selectors

* elements/tags `html` `body` `a`
* classes (for items with shared characteristics)
  * declare: `<tag class="photo menu-item event">content</tag>`
  * select: `.photo` `.menu-item` `.event`
* ids (for unique items)
  * declare: `<tag id="profile_picture">content</tag>`
  * select: `#profile_picture`

#### Embedded
```html
<head>
  <style type="text/css">
    selector(s) {
      property: value; 
    }
  </style>
</head>
```
*Exercise: add a style tag in the head of your index.html then move your inline-styling into it. Next, use a selector to style all the nav items at once.*


#### Style Sheet
```html
<head>
  <link rel=”stylesheet” href=”styles/main.css”>
</head>
```

let's create a stylesheet:

`$ mkdir styles`

`$ touch styles/main.css`

*Exercise: link your stylesheet to your HTML pages and transfer all your styling into it. Now add a univeral style to your html like a background-color. Why might the styles not have been applied to your sub-pages?*