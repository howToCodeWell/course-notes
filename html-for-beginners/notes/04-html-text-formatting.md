Paragraphs can contain all sorts of formatted text such as strong text which convays importance, italic text which is used to emphasize the content. 

There are others which are outlined below.

## The difference between bold and strong HTML text

The browser doesn't give any greater importance to bold text however it is rendered in a bolder font than normal text.
Strong tags `<strong>` on the hand are seen by the browser with greater importance and are also rendered in a bolder font.
```html
<p>
    This text is not bold but <b>This text is bold</b>
</p>
<p>
    This text has normal importance <strong>This text has greater importance and is displayed in bold</strong>
</p>
```
## Highlighting text in HTML

Offline paper documents can be marked using highlighter pen. A similar highlight can be marked on HTML documents using the mark element.
```html
<p>
    <mark>This text is is marked</mark>. The browser highlights marked tags
</p>
```
## Changing the HTML mood

The mood or voice of a HTML documents text can be changed using the `<i>` or `<em>` element.

```html
<p>Peter didn't see where he was going and walked into a wall and yelled <em>Ouch</em> in pain.  What a  fool he is</p>
Screen readers will pronouce text with <i> or <em> tags with more emphasis and verbal stress.
```
