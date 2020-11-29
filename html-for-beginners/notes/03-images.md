---
course_slug: html-for-beginners
tutorial_number: 3
type: note
---
In the third HTML tutorial we cover the image tag and how to add images to web pages.

The image tag is called `<img>` and it is a self closing tag. Here is an example

```html
<img src="/path/to/image/file.jpg" />
```
The src attribute holds the path to the image file on the server. This could also be an external path to a remote image.  
```html
<img src="https://www.somesite.com/path/to/remote/file.jpg" />
```
The image tag can also have an alternative text attribute like so:

```html
<img src="/path/to/image/file/jpg" alt="This is an example image" />
```
The alternative text is used by screen readers and it is also displayed on the page when the image cannot be found.
