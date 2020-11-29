---
course_slug: html-for-beginners
tutorial_number: 6
type: transcript
---
[00:00:00] Hello, and welcome to the sixth part of the HTML tutorial series. Today, we're going to look at tables and, um, advanced table features, one of which is nesting in tables. So that's where you have a table within a table. Now, this was a very useful back in the HTML four days where things like CSS. And, um, you know, style sheets and even Java script, uh, wasn't really, um, useful enough as useful as it is today, at least for designing and laying out and positioning elements on the page.

[00:00:41] So. Back in the day, uh, H uh, sorry, tables were nested within each other. Um, and that allow designers to control where certain items off the page, certain elements on the page, uh, where, so for example, if you had it. Border around your page, you could use a table and you could use the table columns as a way of creating that border.

[00:01:08] Um, also you could as B, because you could nest infant nest data within each within itself, you were able to, um, construct. Very complicated layouts and you can use the, uh, the, the percentages to adjust the height and the width and so forth. So that allowed designers, uh, to create, um, well, pretty half decent looking web pages back then.

[00:01:36] Now we've got CSS and Java script. It's far easier and far better to design, um, uh, web pages. But, I mean, essentially what was going on was that, uh, uh, people were using tables in the wrong way. Tables were supposed to just display tablet, data, but often designers used them to, uh, design and layout the page.

[00:02:02] But. Saying that nested tables still have their place today. Um, especially if you've got a lot of complicated data and you wish to isolate certain elements within your template within your table. And, um, you want to, um, uh, but I have almost like a subset in your, uh, in your tablet data. So let's get into it.

[00:02:25] Let's create some nested tables. So what I'm going to do is copy the, um, Uh, tutorial five. So we're going to copy that and put it into two or six. If you haven't seen tutorial five yet I do recommend checking that out because it'll give you some more information that will prove helpful for this one. So I'm going to change some bits and pieces.

[00:02:47] So HTML tutorial, six instead of five, how to nest. Whoops, nest tables in HTML. And, um, uh, here, I'm going to just change this description to, uh, [00:03:00] this tape tutorial demonstrates how to, uh, nest tables in HTML that will do Oh, K let's just save that and bring up. Um, Safari again and refresh this page. We should now have, uh, this page.

[00:03:18] Yeah, that's good. It's um, pretty much the same as what was in the, um, the fifth tutorial. I've just changed the descriptions and the title here. So what we're going to do is we're going to nest a table within one of these table cells. In fact, we're just going to use this one. For instance, we're going to remove the word PHP book and we're going to actually have.

[00:03:38] A separate table, a sub table within this primary table. So let's do that. Let's go back into here. Let's remove where it says, uh, products up, sorry, here, where it says PHP book. And what we're going to do is just create a new table within that. So table, and then close that off, create our table row and close that off too.

[00:04:04] And we need a T H because of the table header. And in here, we're going to just have the word test header, like, so, and let's just bring that down a wee bit so we can see more information. Next thing I'm going to do is like before is create another table row. And in that I'm going to have a bunch of TDS.

[00:04:28] Well, for now, I'll just have one. So TD. TD. So that's the table cell. And in here, I'm going to just have test cell like that. Let's save that and, uh, just double check that. Yep. That looks good. So let's open up Safari again and refresh the page. So we've got this, uh, this new. Table. It doesn't actually look like a table at the moment because it just looks like we've got one line here and then perhaps a line break and another one.

[00:04:59] But actually, if I was to copy that or highlight the whole thing, you can see that there is two table cells here. This is the table header and the table cell itself. So, um, as before, because we haven't defined the width. It's just going to use the width of whatever the content is. So we can actually change that.

[00:05:20] Um, let's go back into here and change the table width. So let's do width is equal to, and we're going to do 50%. I'm going to save that and go back into here. Refresh this. And can you see that we've got, um, a, uh, uh, 50% of the products bit here has been consumed by this, uh, table, this sub table. And I can change that to be a hundred percent and it will consume all of that as well.

[00:05:55] Let's go back into Safari, refresh the page. Um, we can see that it's consumed all of it. Now, the reason why this here has, um, there's some space here is because there is space in all of these tables and that is due to the cell padding. Now the cell padding is set on the parent table, this, um, base table here.

[00:06:19] Let's go back into here. Change the cell padding from 10. We're going to make that zero, save that, go back into Safari, refresh the page. And it's all, uh, butted up to the end like that. Okay. Let's um, let's put in some borders in the sub table. So border is equal to one. Save that. Okay. So we have a border in a sub table.

[00:06:53] Now notice as I'm doing this, it's not actually inheriting the, um, the, uh, attributes of the parent table, um, which is something that CSS does because it, CSS is a custom cascading style sheet. I'll get into CSS in a lot more. Detailed down the road. Uh, but it's, uh, one thing that, um, you know, this doesn't do and that is inherit the properties of the base table, which is a good thing.

[00:07:22] Um, let's go back into here. Let's use an attribute that we haven't actually used before, and that is changing the background color. So what we can do is do BG. Color and it's Americanized. So it's, um, color is spelled C O L M O R. And we can either use a hex for dense decimal code, or we can actually use it or an RGBA or we could use just a word that represents the color.

[00:07:54] So for example, red, and let's save that. Go back into Safari, refresh the page and you can see everything has turned red. Now what we can do because, um, by default the table, uh, color is transparent, which means it doesn't actually have a color. Um, We can change this one here and we can change the sub, the sub table to be a different color to the color of the parent table.

[00:08:24] Um, let's try that now. Let's change this one to be a BG color. Of, I don't know, let's change that to be a blue, like, so, and go back into here and we could see now it's all blue. So that's blue and that's red. Um, okay. And if I was to change, uh, was if I was to remove this one from red.

[00:08:53] And go back into here, refresh the page. Then this is only blue that has gone  back to transparent, which is white. And it's transparent because if I was to change the, uh, the color of the. Background of the actual page, which again, is something that I'll get into in the CSS tutorials down the line. Then this table would also change its color to the background as well.

[00:09:17] In fact, it's not actually changing the tables background because the background is transparent. So whatever the color is, or the images behind this table will also be shown through. Okay. So that was a, uh, a quick tutorial, really on nesting tables. So that's where you have a table within a table. Like I said, this was very useful back in the HTML four days, but, uh, that, um, you shouldn't, shouldn't be, uh, creating.

[00:09:46] Nesting tables for layouts anymore. CSS is the way to go, but there are still times where nesting tables is pretty useful, especially if you've got a lot of data and you want to break down some of that data into smaller individual. Subsets. Um, perhaps though I would suggest that if you weren't in, in having to do that, then perhaps look at creating another page with a subset of data in that, and perhaps use links to, and fro those pages.

[00:10:18] Otherwise you see, uh, the code will be getting quite complicated because you can nest tables as many times as you want. And if you look here. You've, you know, th the, for nesting level here is, is pretty deep and it'll get deeper. The further you go down, because the thing is tables. Aren't just, um, one level deep.

[00:10:40] Now, just two levels, deep, deep, but they're often three or four levels deep. So for example, table tr T H. So, you know, If you're nesting a new table, then you've got, you're automatically adding three other additional layers of tax tags or tech net nesting as it's called. Okay. I'm going to leave it there, but if you've got any questions, then do let me know, subscribe to get the next tutorials and the web chats every week.

[00:11:10] Um, like the video, if you found it helpful and do share it and share it around, if you think others. Might do as well. Thanks again for watching and I'll see you again next time. Thank you. Bye.
