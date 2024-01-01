## How websites work
* When you visit a website, your browser makes a request to the web server asking for info about the page you're visiting
* The web server responds with data that your browser uses to show you the page
* Web server: dedicated computer that handles your request
* Two major components that make up a website
  * Front end: the way the browser renders the page
  * Back end: server that processes your request and returns a response
 
## HTML
* Websites are created using HTML, CSS, and JavaScript
* HTML defines the structure of the website, CSS styles the website, and JavaScripts adds functionality & interactivity
* Elements are the building blocks of HTML (HyperText Markup Language) pages and tells the browser how to display content

Here's an example:
```
<!DOCTYPE html>
<html>
  <head>
    <title> Page Title </title>
  </head>
  <body>
    <h1> Example Heading </h1>
    <p> Example Paragraph </p>
  </body>
</html>
  ```

* ` <!DOCTYPE html>` defines that the page is a HTML5 document
* `<html>` element is the root element of the HTML page - all other elements come after this element
* `<head>` element contains information about the page (such as the page title)
* `<body>` element defines the HTML document's body; only content inside of the body is shown in the browser
* `<h1>` element defines a large heading
* `<p>` element defines a paragraph
* Tags contain attributes such as the class attribute which can be used to style an element (`<p class="bold-text">`), or the src attribute which is used on images to specify the location of an image (`<img src="img/cat.jpg">`)

## JavaScript
* JavaScript can be added with the page's source code within the `<script>` tag or with a src attribute `<script src="/location/of/javascript_file.js"></script>`

## Sensitive Data Exposure
* Sensitive Data Exposure occurs when a website doesn't properly protect (or remove) sensitive clear-text information to the end-user
* This data is usually found in a site's frontend source code
* A web developer may forget to remove login credentials, hidden links to private parts of the website or other sensitive data shown in HTML or JavaScript
* Sensitive information can be potentially leveraged to further an attacker's access within different parts of a web application

## HTML Injection
* HTML Injection is a vulnerability that occurs when unfiltered user input is displayed on the page
* If a website fails to sanitize user input, filter any "malicious" text that a user inputs into a website, and that input is used on the page, an attacker can inject HTML code into a vulnerable website
* Input sanitization is helpful in keeping a website secure, as information a user inputs into a website is often used in other frontend and backend functionality







