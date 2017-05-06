# The aesthetics of a website

In the *The backbone of a website* challenge we've tried to make a simple website with HTML.

HTML describes *what* elements are to be presented to a user, but is very hard to describe *how* the elements are presented, such as the font, colors, layout etc. Thus, a new language is invented: **Cascading Style Sheets (CSS).**

Let's try to apply CSS to the simple website we made.
1. In the same directory as `index.html` and `about_me.html`, create a new file called `my_style.css`, and put in the following content:
```css
  h1 {
    color: blue;
    font-size: 50px;
  }
```
  Above is called a CSS rule, and every CSS rule contains the following:
  - a selector (`h1`)
  - one or more properties (`color`, `font-size`)
  - value for each of the properties (`blue`, `50px`)

  The CSS rule above selects *all* `h1`s in a HTML document, turn them into blue color, and sets them to 50 pixels big.
2. Open up `index.html` with your browser and you should see all `h1` tags turned blue and enlarged, but it's not!

3. It's not magic. The CSS file (`my_style.css`) and the HTML file (`index.html`) doesn't 'link' together magically. You need to put the following into the `<head>` tag of your HTML file.
```html
  <head>
    <title>Home | My Website</title>
    <!-- the following tag is needed -->
    <link rel="stylesheet" href='example.css'>
  </head>
```
  The `href` attribute tells browser the name of the file to be linked, while the `rel="stylesheet"` attribute tells the browser the relationship between the current file (`index.html`) and the linked file (`example.css`)
