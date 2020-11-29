---
course_slug: html-for-beginners
tutorial_number: 7
type: transcript
---
[00:00:00] Hello, and welcome to the seventh part of the HTML tutorial series. Today, we're going to look at some advanced semantics of a HTML table. There are three elements that I've left out. In my previous HTML table tutorials, these are used to identify the correct portions of a table, and they're used by screen readers for accessibility and other things like that.

[00:00:24] So when a screen reader is reading the contents of the web page, it uses these, uh, these three elements to identify the correct. Areas of, of the table. These are the table headers, the table footers as well as the table body. So T head for the table, header, uh, T body for the, for the body, as well as T foot for the footer of the table.

[00:00:50] Let's get into it. Let's write some code. I'm going to copy tutorial six into tutorial. Seven. Let's save that. And let's change a couple of bits. So HTML tutorial, seven, how to structure? Oops. A table in HTML. And this tutorial demonstrates, um, table structures

[00:01:21] in HTML and a talk on table. Symantec's like, sorry. Okay. Now this, uh, this table that we've got here that I've copied from the previous tutorial has a nested table inside. We're going to remove that for now. And we're going to just change this to be PHP course. Let me bring that up, uh, to a single row, a single line, just to.

[00:01:52] Uh, give us some more room. Let's save that now. Um, let's go into the browser, which is, uh, here and refresh the page. And we can see that we have this, this table, um, for us already created now. Uh let's let's uh, let's talk about this table and how it's semantically created. So we have, um, Uh, four table rows here.

[00:02:16] We have a row here, row, row, and a row. And within these rows we have, uh, three columns. And on the last row, we actually have two columns it's being used. Uh, this one here has a coal span that spans two columns. But, um, we haven't actually written anything that can identify, uh, the actual portions that make up this table.

[00:02:39] So when a screen reader reads this, this a table, it doesn't know what is the header? What is the footer and what is the body of the table? Um, so for example, we would assume that this would be the table heading. Uh, we would assume that this is the table body, and we would assume that this is the table foot, but because we haven't actually.

[00:03:00] Put in those semantic elements, the screen readers don't know this. And so we need to add those elements to the code. So let's go ahead and do that. Now. Let's go back into the code and have a look at what we've got. So we have these TRS T RS, T RS, and a Tiara there that makes the table rows. And within each table row, we have at least two or three table columns.

[00:03:26] So that's a column. That's a column. That's a column and on the S on the last table row, we have two columns here. Uh, this one has a call span of two. Okay. So the table header, the T head can go right at the top here. So we have T whoops T head and like with all tanks, we open it and we close it as well.

[00:03:52] Whoops. Let's put that in here. So closing the T head. Let's save that and move some of these out. So we have a table header straight into the table, sorry, the table straight into the table header. And then we have a single row within this table header, which has these three columns, these three, uh, T hitches.

[00:04:14] Let's save that. I'm going to just move this up a little bit so you can see. Okay. So the next thing we can do is, uh, designate the portion of the table, which will be the table body. And these are the table body in this case has two table rows. So this one, and this one, remember this one down here is the footer of the table.

[00:04:36] So we don't have to worry about that too much at the moment. So what we can do is T body, and we're going to close that off. Like, so let's save that and bring these into line. Oops. Like, so, so we have a table, then we have the table head and then we have the table body. The table head has one row. The table body has two rows.

[00:05:05] Okay. Now the last row here will be art table foot. So that is T foot like, so whoops.

[00:05:21] And the safe let's bring those in line. Like the others. So now you can see that we have a designated three or we've identified the three portions that make up the table. So we have the table tag in here. Let's show you that a little bit more. Um, we have the table head, table, body, and the table foot. But notice if we save this and we go back to the browser, refresh the page, we actually haven't done anything.

[00:05:50] Uh, visually changing to the, the table. We've just added those structural rules, these semantic rules to the code.

[00:06:00] So, um, basically the point I want to make is some code that you write will not actually change the visual. Um, the visual effects of the HTML page, but they used, uh, by the screen readers for things that actually read the screen, um, to, uh, to talk to, well, when the screen readers actually read the elements of the page, they can say that this is the table header.

[00:06:23] This is table body, and this is the table foot. Very important for accessibility. So this is a brief. Brief demonstration and a brief talk of the semantics of that. Make a table. If you've got any comments or questions, do you put them in the comment section below and I will get back to you as soon as I can.

[00:06:42] Um, if you found this video helpful, then do I like the video do share it around. If you think others might find it helpful to subscribe, to pick up the next tutorials and the web chats that I do each week. Thanks again for watching and I'll see you again soon. Thank you. Bye.
