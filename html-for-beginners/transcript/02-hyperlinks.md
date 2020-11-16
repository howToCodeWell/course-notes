[00:00:00] Welcome to another HTML tutorial today, we're going to look at element tags. Element tags are how we can link web pages together. So when a browser sees a tag in the markup in HTML,  it knows that it is a link. Now these links can be links between the pages between the websites. Between web pages or to external pages themselves.

[00:00:24] We're also going to look at attributes within the, a tag as well. Attributes is something that I haven't covered yet in, in the HTML markup. Now, what I'm going to do is create a second HTML page and we're going to call it tutorial two. So as you can see here, we've created a HTML file and it's completely blank.

[00:00:44] And if I was to go back to the index page, this is where we left off last time, which is what we can see here rendered out. So what I want to do first of all just for ease is copy that. Go into the second page, the tutorial two, and [00:01:00] paste that in. I'm going to just change a few things here. Let's just change that to be tutorial two, and I'm going to also change that to be how to link to other pages.

[00:01:13] And I'm just going to give it some texts. So this tutorial demonstrates how to link to other pages using a tax, save that. And we're going to remove this unordered list like, so, and if I was to just to scroll over here, change that to be tutorial too. Um, we can see that we've quickly created that page.

[00:01:50] So how to link to other pages, this tutorial demonstrates how to link to other pages using a tags. Okay. So what I'm going to do [00:02:00] is for quickness is just create a, another paragraph tag and in that paragraph tag, I'm going to nest inside this and a tag and this a tag. Well, we'll open it like, so, and we're going to have, go to tutorial one.

[00:02:22] So now we need to give this a tag a series of attributes or an act, a specific attribute called the H ref attribute. And this attribute will hold the value of the file that we wish to link to in this case, the very first tutorial, which is called index well, HTML. Okay so let's do that now.

[00:02:44] So attributes go within the tag declaration. So H ref. And we can equal that to a string and that string will have a index dot HTML and [00:03:00] save that. Okay. That looks good let's render that out and there we go. See, we've got this new paragraph tag and in that paragraph tag, we have a nested, a tag and in the eight annd we have attribute of index dot HTML, go to tutorial one now without this, it will completely fail.

[00:03:24] If I was to save that, refresh the page. Can you see that the underline has been removed? If I was to put it back, we can now see, see that it's back again. And it's also changed color. Now this is basically, this means that the browser has realized that this is an, a tag and has rendered it. As a link. And if I, if whoops, if I was to click that, we now go back to the first tutorial.

[00:03:50] And likewise, if I was to put that in here, so we go back into the index, come on. Oops. [00:04:00] Ah, um,

[00:04:08] Thank you. Right. If we went back in here and we pasted that in and we did go to tutorial two, and we changed that to be to Tori. Real two and save that, refresh this page, and we can see the go-to tutorial to go to tutorial one and so forth. Now this is very good for, um, creating menus. So your head navigation or your links, um, and normally what happens is that this actually goes in.

[00:04:43] Two, if we're creating a sidebar, for example, a unordered list. And we would have L I L I, and in here we would have this tag here go to tutorial two. And I'm just going to do tutorial save that. Yeah. Just double check. That looks good.

[00:05:11] Refresh the page and there we go. And I've actually nested the, a tag within the Alliance. So we, what we've got here is essentially three nests. So the UL is nested within the body. In fact, for nests because the UL is in the body, the body is within the HTML. The AA is within the ally, which is inside the UL.

[00:05:31] And if we had lots and lots of, um, of, of tutorials, which I hope we will have future in the future, we can have lots and lots of, um, or unordered list items, items here, each having their own, a tag, like, so, okay. This, uh, this is a very quick tutorial on linking internal pages together now. Um, As I've demonstrated this P this, [00:06:00] this link refreshes the actual page, but what happens if you want to keep the page?

[00:06:06] Um, but you, that you currently are on existing. What happens if, for example, you want to create a new tab? Well, you would do that by designating a new attribute called target. Um, like, so target is equal to, and then again, it's a string and an insight here we would do underscore blank. Now what that means.

[00:06:28] Is when the, uh, when, when the browser renders this page sees that this isn't a tag, it sees that that is the link that the hatred, that's the link in which it's going to, but this target basically means that, um, it goes to a new tab, a blank tab, underscore blank. Let's save that. Refresh this page. Double check.

[00:06:51] Yeah, go to tutorial. Two lots. I'm on the right one and hit that now. Notice. That we've actually created [00:07:00] a second tab here in the browser. Um, she, that, so we've, we've clicked on go-to tutorial too, and that's actually created a new tab. Like, so if we were to remove, if we were to remove the target, it would just go like normal.

[00:07:22] Why was to refresh that? And hit that, then we would just change the page. Now what also, what we can do is link to external resources. So we can actually link to external pages. Let's say, for example, we wanted to go to, uh, the, one of the Twitter, my Twitter profile. So let's just create, um, uh, one here.

[00:07:45] Let's just do another, I'm going to do another ally. Okay.

[00:07:53] So follow PF WT on Twitter. Yeah, that's correct. And just by, um, memory, I'm going to try and remember the URL. So there'll be ww.twitter.com forward slash. PF WD, I want to have this go into a new page because, um, instead of, uh, a new tab, instead of, instead of refreshing this page, I don't want to take the user away from this website that I'm creating.

[00:08:33] And therefore I would do target equals underscore blank, like, so, okay. So we've got this, a tag here. Um, it got the target of underscore blank. This is the HRF, um, and the text is follow P FWD on Twitter. Let's just save that and refresh this page. We should have, um, whoops, I [00:09:00] need to go back here. There we go.

[00:09:01] So we've got these two links here. Tutorial two. We'll just refresh this page, going back to the second tutorial and this one here should. Open up a new page like it does, and then loads up the PFDD Twitter profile like that. Um, okay. Let's just go back and you can see, like I mentioned before, this is very useful for creating menus and things.

[00:09:32] So you would have like a sidebar of links, um, Uh, well, and that go to various places on your website, as well as other websites, uh, other resources and so forth. Okay. So this is a very basic tutorial of linking in HTML. If you found it useful, then do like the page, like the, like the video as well as share it around.

[00:09:55] If you think others might find it useful too. Um, if you've got any comments or questions, then leave them in the comment section below and I'll try and get back to you as soon as I can do subscribe, because there'll be many more tutorials like this to come as well as the Friday web chats. Thanks again for watching.

[00:10:11] And I shall see you again soon.