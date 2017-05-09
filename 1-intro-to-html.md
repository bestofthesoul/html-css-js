# The backbone of a website

## What is a HTML (Hyper Text Markup Language) document?

Every webpage that you visit is written in a language called Hyper Text Markup Language, or HTML in short. This is the skeleton or structure that forms the foundation of every web page. Though, without a browser, a HTML file is just a *normal text file*.

> Web browsers (Google Chrome, Mozilla Firefox, Safari, Opera etc.) can understand HTML files and is able to render those files into what we see on websites.

Let's try to make a simple website of your own now:
1. Create a file called `index.html` with the following content:
    ```html
    <!DOCTYPE html>
    <html>
      <head>
        <title>Home | My Website</title>
      </head>
      <body>
        <h1>My Website</h1>
        <h2>I made this</h2>
      </body>
    </html>
    ```
2. Open the file with your browser (Chrome, Firefox, Safari etc.)

  There you go! You have made your own website! Except this website now is not associated to a public domain, and thus can only be accessed through your computer. The address bar (where you see the link of the website) shows the location to your html file.

3. Let's move on and add another page to your website! Create **another file** under the same directory with `index.html`, name it `about_me.html`, and insert the following into the file:
    ```html
    <!DOCTYPE html>
    <html>
      <head>
        <title>About me | My Website</title>
      </head>
      <body>
        <h1>About me</h1>
        <h2>My name is Josh and this is a webpage I made in Next Academy! </h2>
        <p>It doesn't look very nice now. But I will try my best to make it look good!</p>
      </body>
    </html>
    ```
    You can replace "Josh" with your own name, obviously. It's your website after all.

4. Open this file with your browser again. You've made another page!
5. You probably realize if you want to go back to your homepage again you'll have to click on `index.html` again. That's not nice! Let's add a clickable link into `about_me.html`
    ```html
    <!DOCTYPE html>
    <html>
      <head>
        <title>About me | My Website</title>
      </head>
      <body>
        <h1>About me</h1>
        <h2>My name is _____ and this is a webpage I made in Next Academy! </h2>
        <p>It doesn't look very nice now. But I will try my best to make it look good!</p>
        <a href="index.html">Click here to go back to homepage</a>
      </body>
    </html>
    ```
6. Open `about_me.html` again and you should see a link in blue. Click on it and you should be redirected back to the homepage.

You can also proceed to add an `<a>` tag into `index.html` to generate a link to `about_me.html` as follows:
```html
<!-- You can add comments like this in HTML -->
<a href='about_me.html'>About me</a>
```

## HTML tags
An example of a HTML tag looks like this
```html
<h1>Hello World</h1>
```
It contains
- an opening tag: `<h1>`
- a closing tag: `</h1>`
- `h1` is used to indicate that the content between the opening tag and closing tag, is a first class header.

However, some HTML tags may not need a closing tag.
```html
<input>
<br>
```

You can even make your own HTML tags!
```html
<cool></cool>
```

Some HTML tags requires specific *attributes* to work.
```html
<a href="https://www.google.com">Go to Google</a>
<img src="https://placehold.it/350x150">
```

You can also put a HTML tag inside another HTML tag.
```html
Click the Facebook Logo to visit NEXT Academy's page!
<a href="https://www.facebook.com/getschooledbynextacademy/">
  <img src="https://members.aavmc.org/style%20library/aavmc_branding/img/facebook.png"/>
</a>
```
An `a` tag in a HTML will be turned into a link in your website when rendered by browsers. When user clicks on the link, the browser will then bring the user to the URL specified in the `href` attribute.

Tags like `h1` and `img` has their own meaning to browsers, while tags you create on your own will not have any effect visually.

Here is a list of HTML tags you can try out
https://www.w3schools.com/Tags/

> Note: Not all tags have visual effect when rendered, some are used for SEO (Search Engine Optimization) or other purposes:

Recommended tags to try and combine:
```html
<div>
<img>
<table>, <tbody>, <th>, <tr>, <td>
<input> <!-- different 'types' -->
<select> <option> <textarea>
<a>
<ul>, <ol>, <li>
<strong>, <em>
```

You can play around with `index.html` and `about_me.html` by trying out/adding more different `HTML` tags, or even add more `HTML` pages. But you'll soon notice that you can add more to the *structure* of the website, but not much to the *aesthetics* of the website. This is where CSS comes into play! Give yourself a short **10-15 minutes** to discover HTML and proceed to the *NEXT* challenge.

> Fun fact 1: Unlike Ruby, even if a HTML document has syntax errors, browser will not raise an error and stop rendering. This is intended so that normal users will not have to see ugly, hard-to-understand error messages. Though, this can make a HTML code hard to debug at times.

<br>

> Fun fact 2: You can make a link that opens in a new tab like this
```html
<a href="https://www.google.com" target="_blank">Google in new tab!</a>
```
