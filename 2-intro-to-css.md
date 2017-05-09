# The aesthetics of a website


## Introduction

In the *The backbone of a website* challenge we've tried to make a simple website with HTML.

HTML describes *what* elements are to be presented to a user, but is very hard to describe *how* the elements are presented, such as the font, colors, layout etc. Thus, a new language is invented: **Cascading Style Sheets (CSS).**


## Hands-on!

Let's try to apply CSS to the simple website we made.
1. In the same directory as `index.html` and `about_me.html`, create a new file called `my_style.css`, and put in the following content:
```css
  h1 {
    color: blue;
    font-size: 50px;
  }
```
  This is called a CSS rule, and every CSS rule contains the following:
  - a selector (`h1`)
  - one or more properties (`color`, `font-size`)
  - value for each of the properties (`blue`, `50px`)

  The CSS rule above selects *all* `h1`s in a HTML document, turn them into blue color, and sets them to 50 pixels big.
2. Open up `index.html` with your browser and you would expect to see all `h1` tags turned blue and enlarged, but it's not!

3. Of course, the CSS file (`my_style.css`) and the HTML file (`index.html`) doesn't *link* together magically. You need to put the following into the `<head>` tag of your HTML file.
```html
  <head>
    <title>Home | My Website</title>
    <!-- the following tag is needed -->
    <link rel="stylesheet" href='example.css'>
  </head>
```
  The `href` attribute tells browser the name of the file to be linked, while the `rel="stylesheet"` attribute tells the browser the relationship between the current file (`index.html`) and the linked file (`example.css`).

  Now you should see the content inside all `h1` tags follows the CSS rule.

## Classes and IDs

With the CSS rule above, **every single `h1`** tag will turn blue and enlarged to `50px`. What if you just want certain `h1` tags to have that rule? Rather that selecting particular tags in a CSS rule, you can use `class` for that matter.

### Class
Say you have a HTML document that looks like this:
  ```html
    <!DOCTYPE html>
    <html>
      <head>
        <title>Home | My Website</title>
      </head>
      <body>
        <h1 class='big-blue-header'>My Website</h1>
        <h2>I made this</h2>

        <h1>My Journey</h1>
        <h2>It's been good so far</h2>

        <h1 class='big-blue-header'>Conclusion</h1>
        <h2>I love to code</h2>
      </body>
    </html>
  ```
  You can apply the CSS rule to `h1` tags that has a class `big-blue-header` this way:
  ```css
    .big-blue-header {
      color: blue;
      font-size: 50px;
    }
  ```

  Refresh your page and the text `My Website` and `Conclusion` should now turn blue.

  By seperating the class names with a space, a HTML tag can have multiple classes:
  ```html
  <h1 class='big blue'>My Website</h1>
  <p class='big'>Conclusion</p>
  ```

  This way, your CSS could look like this:
  ```css
  .big {
    font-size: 50px;
  }

  .blue {
    color: blue;
  }
  ```

### ID

While you can use `class` to group multiple HTMl tags together and use it for CSS rules, `id` specifies a unique id for a **single HTML tag/element4**. In other words, there should not be 2 elements that has the same `id`.

A example of a HTML element with an `id`:
```html
<h2 id="angry-rant">Classes and IDs are confusing!</h2>
```

CSS rule to select `id`:
```css
#angry-rant {
  color: red;
  font-size: 100px;
  font-weight: bold;
}
```

> Small note: You can try making two elements have same `id`, and your CSS rule will be applied to both elements.
