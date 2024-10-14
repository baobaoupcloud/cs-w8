---
title : "Regular Expressions"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
***Regular expressions*** or regexes are a means by which to ensure that user-provided data fits a specific format.

We can impelement our own registration page that utilizes regexes as follows:
```html
<!DOCTYPE html>

<!-- Demonstrates type="email" -->

<html lang="en">
    <head>
        <title>register</title>
    </head>
    <body>
        <form>
            <input autocomplete="off" autofocus name="email" placeholder="Email" type="email">
            <button>Register</button>
        </form>
    </body>
</html>
```
Notice that the input tag includes attributes that designate that this is of type email. The browser knows to double-check that input is an email address.

While the browser uses these built-in attributes to check for an email address, we can add a pattern attribute to ensure that only specific data ends up in the email address:
```html
<!DOCTYPE html>

<!-- Demonstrates pattern attribute -->

<html lang="en">
    <head>
        <title>register</title>
    </head>
    <body>
        <form>
            <input autocomplete="off" autofocus name="email" pattern=".+@.+\.edu" placeholder="Email" type="email">
            <button>Register</button>
        </form>
    </body>
</html>
```
Notice that the pattern attribute is handed a regular expression to denote that the email address must include an `@` symbol and a `.edu`.