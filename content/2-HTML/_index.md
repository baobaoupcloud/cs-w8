---
title : "HTML"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
***HTML*** or hypertext markup language is made up of tags, each of which may have some attributes that describe it.
In your terminal, type code hello.html and write code as follows:

```html
<!DOCTYPE html>

<!-- Demonstrates HTML -->

<html lang="en">
    <head>
        <title>hello, title</title>
    </head>
    <body>
        hello, body
    </body>
</html>
```
Notice that the `html` tag both opens and closes this file. Further, notice the `lang` attribute, which modifies the behavior of the `html` tag. Also, notice that there are both `head` tags and `body` tags. Indentation is not required but does suggest a hierarchy.

You can serve your code by typing http-server. This serve is now available on a very long URL. If you click it, you can visit the website with your own code.

When you visit this URL, notice that the file name hello.html appears at the end of this URL. Further, notice, based upon the URL, that the server is serving via port 8080.

The hierarchy of tags can be represented as follows:

![Hierachy](https://raw.githubusercontent.com/baobaoupcloud/cs-w8/main/static/images/2.html/html1.png)

Knowledge of this hierarchy will be useful later as we learn JavaScript.
The browser will read your HTML file top to bottom and left to right.
Because whitespace and indentation is effectively ignored in HTML, you will need to use `<p>` paragraph tags to open and close a paragraph. Consider the following:

```html
<!DOCTYPE html>

<!-- Demonstrates paragraphs -->

<html lang="en">

    <head>
        <title>Headings</title>
    </head>

    <body>
        <p>
            This is a sample text that demonstrates the use of headings. It includes various elements to showcase formatting and structure.
        </p>
        <p>
            This section continues to illustrate the use of headings, providing more details and examples in a structured manner.
        </p>
        <p>
            Here we delve deeper into the content, highlighting additional information that supports the main topics discussed.
        </p>
        <p>
            As we go further, this section emphasizes key points and introduces relevant insights that complement the previous sections.
        </p>
        <p>
            This subsection contains important notes and considerations that readers should keep in mind as they explore the topic.
        </p>
        <p>
            Finally, this section wraps up the discussion, summarizing the essential takeaways and providing final thoughts on the subject.
        </p>

    </body>
</html>
```
Notice that paragraphs start with a `<p>` tag and end with a `</p>` tag.

HTML allows for the representation of headings:
```html
<!DOCTYPE html>

<!-- Demonstrates headings (for chapters, sections, subsections, etc.) -->

<html lang="en">

    <head>
        <title>Headings</title>
    </head>

    <body>

        <h1>One</h1>
        <p>
            This is a sample text that demonstrates the use of headings. It includes various elements to showcase formatting and structure.
        </p>

        <h2>Two</h2>
        <p>
            This section continues to illustrate the use of headings, providing more details and examples in a structured manner.
        </p>

        <h3>Three</h3>
        <p>
            Here we delve deeper into the content, highlighting additional information that supports the main topics discussed.
        </p>

        <h4>Four</h4>
        <p>
            As we go further, this section emphasizes key points and introduces relevant insights that complement the previous sections.
        </p>

        <h5>Five</h5>
        <p>
            This subsection contains important notes and considerations that readers should keep in mind as they explore the topic.
        </p>

        <h6>Six</h6>
        <p>
            Finally, this section wraps up the discussion, summarizing the essential takeaways and providing final thoughts on the subject.
        </p>

    </body>
</html>
```
Notice that `<h1>`, `<h2>`, and `<h3>` denote different levels of headings.

We can also create unordered lists within HTML:
```html

<!DOCTYPE html>

<!-- Demonstrates (ordered) lists -->

<html lang="en">
    <head>
        <title>list</title>
    </head>
    <body>
        <ul>
            <li>foo</li>
            <li>bar</li>
            <li>baz</li>
        </ul>
    </body>
</html>
```
Notice that the `<ul>` tag creates an unordered list containing three items.

We can also create ordered lists within HTML:
```html
<!DOCTYPE html>

<!-- Demonstrates (ordered) lists -->

<html lang="en">
    <head>
        <title>list</title>
    </head>
    <body>
        <ol>
            <li>foo</li>
            <li>bar</li>
            <li>baz</li>
        </ol>
    </body>
</html>
```
Notice that the `<ol>` tag creates an ordered list containing three items.

We can also create a table in HTML:
```html
<!DOCTYPE html>

<!-- Demonstrates table -->

<html lang="en">
    <head>
        <title>table</title>
    </head>
    <body>
        <table>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr>
                <td>4</td>
                <td>5</td>
                <td>6</td>
            </tr>
            <tr>
                <td>7</td>
                <td>8</td>
                <td>9</td>
            </tr>
            <tr>
                <td>*</td>
                <td>0</td>
                <td>#</td>
            </tr>
        </table>
    </body>
</html>
```
Tables also have tags that open and close each element within. Also, notice the syntax for comments in HTML.

Images can also be utilized within HTML:
```html
<!DOCTYPE html>

<!-- Demonstrates image -->

<html lang="en">
    <head>
        <title>image</title>
    </head>
    <body>
        <img alt="photo of bridge" src="bridge.png">
    </body>
</html>
```
Notice that `src="bridge.png"` indicates the path where the image file can be located.

Videos can also be included in HTML:
```html
<!DOCTYPE html>

<!-- Demonstrates video -->

<html lang="en">
    <head>
        <title>video</title>
    </head>
    <body>
        <video controls muted>
            <source src="video.mp4" type="video/mp4">
        </video>
    </body>
</html>
```
Notice that the type attribute designates that this is a video of type mp4. Further, notice how controls and muted are passed to video.

You can also link between various web pages:
```html
<!DOCTYPE html>

<!-- Demonstrates link -->

<html lang="en">
    <head>
        <title>link</title>
    </head>
    <body>
       Visit <a href="https://www.harvard.edu">Harvard</a>.
    </body>
</html>
```
Notice that the `<a>` or anchor tag is used to make Harvard a linkable text.

Meta tags are used to hold information about the data within the HTML file. Consider the following:
```html
<!DOCTYPE html>

<!-- Demonstrates responsive design -->

<html lang="en">
    <head>
        <meta name="viewport" content="initial-scale=1, width=device-width">
        <title>meta</title>
    </head>
    <body>
        This is placeholder text used in design and publishing to fill in content areas with random Latin-based words.
    </body>
</html>
```
Notice this set of meta attributes makes this page mobile-friendly.

There are numerous meta key-value pairs that you can use:
```html
<!DOCTYPE html>

<!-- Demonstrates Open Graph tags -->

<html lang="en">
    <head>
        <meta property="og:title" content="CS50">
        <meta property="og:description" content="Introduction to the intellectual enterprises of computer science and the art of programming.">
        <meta property="og:image" content="cat.jpg">
        <title>meta</title>
    </head>
    <body>
        ...
    </body>
</html>
```
Notice that these key value pairs relate to the title and description of the web page.

You can also create forms reminiscent of Google’s search:
```html
<!DOCTYPE html>

<!-- Demonstrates form -->

<html lang="en">
    <head>
        <title>search</title>
    </head>
    <body>
        <form action="https://www.google.com/search" method="get">
            <input name="q" type="search">
            <input type="submit" value="Google Search">
        </form>
    </body>
</html>
```
Notice that a form tag opens and provides the attribute of what action it will take. The input field is included, passing the name q and the type as search.

We can make this search better as follows:
```html
<!DOCTYPE html>

<!-- Demonstrates additional form attributes -->

<html lang="en">
    <head>
        <title>search</title>
    </head>
    <body>
        <form action="https://www.google.com/search" method="get">
            <input autocomplete="off" autofocus name="q" placeholder="Query" type="search">
            <button>Google Search</button>
        </form>
    </body>
</html>
```
Notice that autocomplete is turned off. autofocus is enabled.

We’ve seen just a few of many HTML elements you can add to your site. If you have an idea for something to add to your site that we haven’t seen yet (a button, an audio file, etc.) try Googling “X in HTML” to find the right syntax! Similarly, you can use cs50.ai to help you discover more HTML features!
