---
course_slug: html-for-beginners
tutorial_number: 2
type: note
---
HTML documents can be linked together using Hyperlinks.  These HTML elements are defined using a tags:

```html
<a href="https://www.howtocodewell.net">Link text</a>
```

The most important attribute that the hyperlink has is the href attribute as this contains the hyperlinks destination. The destination can be to a page within the current website.  This is call a local or relative link.  The desitination can also be to an external web page which is called an absolute link.

## Hyperlink targets

A hyperlink has a target attribute that controls how the link is to be opened.  The syntax is as follows
```html
<a href="https://howtocodewell.net/courses" target="_blank">link text</a>

<a href="https://howtocodewell.net/courses" target="_self">link text</a>

<a href="https://howtocodewell.net/courses" target="_parent">link text</a>

<a href="https://howtocodewell.net/courses" target="_top">link text</a>
```

- When the target is set to `_self` the new document will be opened in the current window or tab. This is the default target behavior.
- When the target is set to `_blank` the new document will be opened in a new window or tab.
- When the target is set to `_parent` the new document will be opened in the parent frame.
- When the target is set to `_top` the new document will be opened in the full body of the window.

## Relative URLs

A URL can either be relative or absolute. An absolute URL includes the full web address wherea a relative URL is a local reference whcih doesn't include the HTTP(S) part of the address.
```html
<a href="https://howtocodewell.net/courses">This is a absolute URL</a>

<a href="/courses">This is a relative URL</a>
```

## Titles and tool tips

Hyperlinks can also contain tooltips. These are automatic popups that are displayed when the user hovers over the link.

The contents of these tooltips are contained in the title attribute
```html
<a href="https://howtocodewell.net/courses" title="This text will be displayed when the user hover overs this link">How To Code Well courses</a>
```
