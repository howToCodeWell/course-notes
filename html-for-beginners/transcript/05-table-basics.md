[00:00:00] Welcome to the fifth HTML five tutorial in this basic HTML five series today, we're going to look at tables, how we can create a table and, uh, how we can display a table in HTML. Now, tables in HTML require lots of nested tasks. So I'll go through this slowly and methodically, hopefully at the end of it, we'll have some nice tables.

[00:00:20] Um, to show now what I've done is I've created a tutorial, five dot HTML file here, and the browser is pointing to that file. There's nothing in it at the moment. What I'm going to do is just jump to let's just use the fourth one. This is the tutorial that we did before about, um, formatting text. Let's copy that, put that in to the fifth, uh, file.

[00:00:44] Let's save that. Change that to be five. Oops, not 45 blimey five. Uh, this is going to be how to create tables in

[00:01:00] HTML. And I'm going to remove this paragraph and this pre tag, and here I'm just going to type in, okay. Whoops. This, uh, tutorial. Demonstrates how to create tables in HTML, and we're going to save that.

[00:01:27] Okay. So let's begin. Let's refresh this to see what we've got. Now, what we want to do is create a table between this paragraph and this unordered list here. And we start by using the table tag, which is like, so now the table tag requires some nested table rows. Essentially what you do is you, you construct your table rows and then within those table rows, you create some table cells.

[00:01:56] And there are two different types of table cells that you can add. The first is table heading. And then the second is just a normal table table cell. Um, the table heading has some different, um, uh, style properties to the other tables table cells. Um, and, and I'll just demonstrate that now it's the first thing you need to do is to create our table rows.

[00:02:20] And we do that using T R like, so. And then within the table row. So we're creating the header here where we create we're creating first row of, of table cells, which would be the header. So the, the table headers are T H sorry, T H like that. And we can, I'm going to just put them on a single line for now, and we're just going to have header one and we're going to do, we're going to have three, three Halla headers, one.

[00:02:54] Two three. I'll just change this to two and we'll change that to three, save fat. Now let's refresh this and see what happens already. Okay. So we've got this, um, we've got this row. Of of three columns. So three table, um, table columns had a one, had a two and had a three. This is a row. These are the columns, the table headers.

[00:03:20] So what we can do is create our second row and what's, and also create table cells for each of these headers that go that correspond to each of these headers. So we would create another table row with another three table cells. So T R

[00:03:41] T D. Um, and then we do a nurse. Do you sell one?

[00:03:56] And what I'll do just for ease of, of space. I'm just going to put these up in a single row. It doesn't really matter if it's not on a single row or, or doubled.

[00:04:09] Cell one cell two and cell three. So what we've done is we've created a second table row underneath this, the header, and we've added three table cells, um, that correspond to these table headings. Let's just refresh the page and now we can see, we have these three. I like, so yeah. Now by default, the dimensions of this table is, um, set, um, automatically.

[00:04:38] And basically it's using the width of the, the, the table cells to work out the width of, of how, how far, how wide the table needs to be. So if can you see when I'm dragging my mouse across this, I can, I can actually show you the, the, the gaps between the tables, the table cells, um,

[00:05:00] But we can, what we can do is we can, we can give the, some arguments to the, um, to the table itself to change the dimensions, the width, and the height of the actual table.

[00:05:12] Let's do that now. So let's do width is equal to 100%. And we're going to save that. We're going to refresh the page. And can you see now that the table itself has a hundred percent width that goes spans, right? The way across the page, same with these table headers like that. Can you see that? There's this, this block here and then this block here what's happening is that the, uh, the browser is automatically calculating that we've got three, uh, three.

[00:05:47] Uh, columns and therefore the, uh, it needs to be divided up in such a way that, um, that the balance of width are equal on each of these three, three

[00:06:00] things. Now let's just remove that, for example, uh, for now, because I just wanna demonstrate something else. Let's just refresh that and bring it back to how it was.

[00:06:09] Let's say, for example, we want to change one of these things at the moment. Um, The table headers have the same, um, characters number of characters. And therefore it's going to be the same width, but let's say we want to change one of these. Let's say, um, let's give it a little bit of context. Let's say this is a shopping cart.

[00:06:29] Um, let's say we have, um, a list of, uh, product name products. Yeah. And then we have a list of costs perhaps. Okay.

[00:06:47] And then perhaps we have a list of delivery, delivery charge. Oops. And save that. Let's change this to be, um,

[00:07:00] PHP book. Uh, let's give that a eight costs of 15. Um, or 25 for today's inflation and also have that as two pounds 50. Okay. Save that and refresh the page. Let's see what, how the, um, the whips have changed because we've changed the number of characters in each one of these, that being that the, the one in the middle has the smallest width will be the smallest width.

[00:07:33] Let's refresh the page and notice that we have. Um, products. Um, and then we have the PHP book underneath, but the delivery charge itself is the longest. And also the cell underneath matches the width of, of, uh, the, the table header. Here. Let's go and add another row just to give it a little bit more context.

[00:07:56] So let's move this back here. We're going to have, um, Java script.

[00:08:08] JavaScript course, um, it's going to have zero delivery, but it's going to be 750 full course and let's save that. So now we have a second, um, A row underneath. And even though that's zero, that the actual table cell is the same width as, as that. And then if I was to change this again, to be a width of, let's say a hundred percent, then it works.

[00:08:42] That out as, uh, as, before and notice that the table headers are bold and centered and that's because, uh, the T hitches, excuse me, have a different set of styles, uh, predefined styles that th these TDS do.

[00:09:00] Okay. Um, what else can we do with the whips? Well, we can actually define the whips per, per, uh, a table header.

[00:09:08] So let's say that this is. Um, we're going to remove the width here and let's say that we want products, whoops. To have a width of 50%. So what will happen here is that that becomes 50% with defining this. To be 50% and then the, these will be calculated on the fly. So let's save that and refresh the page.

[00:09:39] Now we can see that this is 50% width of the whole thing. And if I was to change that to be width of a hundred percent, let's save that and refresh the page. Then we can see that the products. Has 50% of the hundred percent width of the, of the table. So the table is a hundred percent of the page products is 50%.

[00:10:04] Um, just to demonstrate, we can change that to be say 75% and these will get even smaller. Like, so he's noticed that, and what we've done here is we've, we've because we've been forced this to be 75% and because the delivery charge itself is too long, it's wrapped itself around. Let's bring that back down to 50.

[00:10:32] Okay. Some other things that I want to demonstrate, um, whoops. Uh, I want to talk about how we can, um, Um, uh, change the amount of, of, um, table columns. Um, in a row. So, uh, at the moment, everything is three columns. So we have, um, products costs and delivery charges. But what happens if for instance, there is, there is two columns, um, instead of, uh, three columns, how do we, um, make ensure that that one column perhaps spans over multiple columns?

[00:11:07] Well, that is possible. Let's um, let's give you an example. Let's create a new table row. Right at the bottom. Um, and let's say that this here is a total and what we want to do is only have two. Um, we want to a table wrote a table columns. So this one here, TD that the total and the, the cost. Um, but if I was to refresh the page, And save that we don't have a row here at all.

[00:11:43] We are sorry, a column here at all, but we do have here and we do have here now. We can ensure that the, this, um, this amount goes here instead of here. And we do that by spanning the first table  across, um, two columns. So we can merge a bit like in a spreadsheet where we can say that we, this, um, this, uh, table column spans.

[00:12:10] Across two columns. And we use something called an argument, an attribute called Cole span. And essentially that is saying that we are spanning across multiple columns. And in this case we want to span across two. So even though, even though we have two columns here, so we've got the TD and the TD here though, the total and, and the price we're saying that this TD spans across two columns.

[00:12:37] So let's save that and refresh. And what we've done is can you see that this column here is spanning straight across, over to, um, this, so, uh, across the products and the costs, um, table as well. And therefore this one goes into the delivery charge. Okay. Another  thing that we can do is we can fiddle around with say the borders.

[00:13:04] So at the moment, borders that we have no borders, but we can have an argument here so we can do border is equal to one. So one pixel let's save that. And refresh the page and notice that we now have borders enabled. Um, and this is a better demonstration, I suppose, of the spanning of the, of the table, um, table columns.

[00:13:28] So the total is spanning across these two. Okay. Another thing that we can do is define the, um, the cell padding and the cell spacing. Now the cell spacing let's work on spacing first. Let's. Change, um, sell ad spelt, sell, sell spacing, and we're going to do is equal to 10. Let's save that. And what that's doing is it's creating, um, spacing between each of these cells.

[00:13:58] So we're not actually changing  that the border is still set to one. And if I was to do that to zero and refresh, we can see that these, we have huge amounts of spacing in between. Okay. So if you're designing a table, then perhaps look at self spacing as a way of, of adding space between the cells. Another thing we can do is something called cell padding.

[00:14:21] Let's let's add that in now. So,

[00:14:28] and we're just going to also add that to 10. Let's refresh this. Okay. Now, uh, cell padding essentially puts padding around the, the, the contents of the, um, of the cells. And it's probably better displayed if I was to change that to be one and refresh. So we can see that we have, um, you see that we've got some spacing in between each section.

[00:14:53] Yeah, I'm sorry. In between each of the, all the content within the, within the cells. If I was to change that to be zero, to just show you what the pattern looks like without the spacing, then, um, there we go. So, okay. Uh, there's a lot more that we can do with tables and I will delve into tables in far more depth in the future tutorials, such as how we can highlight alternative rows, um, and, and other bits and pieces like that.

[00:15:24] Um, when we're looking at the styling and perhaps adding some JavaScript to this as well. Um, and when I talk about. You know, CSS and all that. We're not there yet, but we're, we're, we're slowly getting there. So looking out for those tutorials, if you want to learn some more advanced features of creating HTML tables, but for now, I'm going to leave it like that.

[00:15:45] So if, if, um, if you found this useful than do. Um, give it a thumbs up, uh, share it around. Maybe others might find it useful too. Um, if you've got any comments or questions, if you want more information about how to create tables or if you've got any comments on future videos then, um, or what I should do with future videos, then let me know, put them in the comment section below.

[00:16:08] Thanks again for subscribing, um, and, uh, keep her, keep an eye out for future videos. Thanks again, and I'll see you again soon. Thank you. Bye.
