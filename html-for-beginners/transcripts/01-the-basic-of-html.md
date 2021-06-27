[[00:00:00]]('?time-code=00:00:00') Welcome to the very first HTML tutorial. In this HTML series we're going to talk about the very fundamentals and the basics of HTML. HTML is the cornerstone of web development. Without HTML you literally won't have a web page. This is because HTML stands for Hypertext Markup Language. It is the language that marks up a webpage. So when a browser loads a page, it reads the markup in HTML and decides how the page is to be constructed. In fact, it doesn't make a decision. So in the markup you can designate certain tags to define structural elements and layouts of a web page as well as its content.

[[00:01:01]]('?time-code=00:01:01') So for example you could have headings, you could have paragraphs. The hypertext part of it is the fact that you can link documents or HTML documents together using something called a hyperlink. So you would create a tag called an `a` tag, and that `a` tag will allow you to create a clickable link to one Hypertext markup language document to another and vice versa. So it is, it's essentially a blueprint.

HTML is how the web page is constructed and essentially, strictly speaking, it's not actually a programming language, especially in the same sense as something like a Python or PHP or Java script, because. It is just a way of laying out the page. There's no control flows here. There's no conditional statements. There's no switch statements and it's not object orientated at all. It is quite literally just how the webpage is to be displayed, how it's to be rendered and how the browser interprets it as a web page.

[00:02:19] But like I said, it's the cornerstone of web development. I haven't done a HTML set of tutorials yet. So here we go.

We're going to focus on the fundamentals, the very basics of HTML and how we can actually start constructing HTML to create our own web pages.

[00:02:46] But before I get into that I just want to mention something. Just going through my notes here. I just want to talk about the background of HTML. So HTML was first conceived in the nineties by sir Tim Berners-Lee.

[00:03:10] Around that time version 2.0. I'm going to say version 2.0 because it's a specification and that specification is decided by a group of people in an organization called the W3C.

[00:03:38] You can look it up on the net. Just go to W3C dot org and it lays out how HTML should be used. The reason why we have this organization is that you don't want to have certain browsers going off and doing their own thing. You don't want the browsers, certain browsers to go off and say, you know, I'm going to display my paragraphs in a completely different way to another browser. You need to have some level of consistency throughout the board. Therefore we have W3C. So for every iteration of the versioning the browsers get together with the board and they decide on or they agree on certain specifications.

[00:04:27] And then, um, certain browsers adopt know. Uh, that, that the F the versions or the, the, the. Types the specifications within the version. And then as the later versions of those browsers come out more, um, uh, things get accepted, um, as they're, they're written into the browsers and so forth. So, uh, like I said, back in the 1990s, we had version two.

[00:04:54] Then in 1995 we had version four. Now we're on version five, which came out in, I think it was 19, sorry. It was 2012 that does sound like a long time ago, but HTML five is kind of like the de facto. Now I'm not going to talk any more about previous versions of HTML. There isn't really a point because what's the point in talking about a technology that is no longer used because all the modern day browsers now support HTML five.

[00:05:34] Okay, so let's actually start writing some code. We have on the right hand side here a browser which is Safari and on the left hand side we have a text editor and this text editor in that I'm using is Netbeans. But you can use whatever you want. You could use notepad for example. Just ensure that the file ends with an extension of dot HTML.

[00:05:55] Okay, so the first thing that we need to do is tell the browser what version of HTML that we're using. We use something called a doctype which is the document type. Now in the previous versions of HTML, you would do this in a completely different way. So if for any crazy reason that you're still using an earlier version of HTML. Perhaps HTML 4 for example then do research and Google thatto find out how to do it.

[00:06:22] I'm only focusing on HTML five here and I will be throughout this tutorial series. We do this by creating a doctype which is done like so. This basically means that it is going to be a HTML five document. Now in this document we need to define certain tags and the tags are what creates the page. They are what the browser uses to decide what to and how to render the page out. Within these tags you have the content. So for example, when you're creating a paragraph, you would have a P tag at the start as well as at the end of the paragraph. And the browser would know that that it isa paragraph tag. That markup the paragraph tag. But we need to first open the HTML tag and we do this like so. We also need to close the HTML tag like that. Now opening a tag use the greater than and less than symbols with the the tag name. Then closing them is again the greater than less than symbols, but with this forward slash at the start.

[00:07:48] So that's the start of the HTML document and that's the end of the HTML document. So anything under here is not HTML. The next thing we need to do is actually open up what's called the body. Now the body is what is displayed on the page. Okay, so we have a body there's also a head tag, but I'll get into that in a different video, perhaps another tutorial as we're only worried about the body at the moment.

[00:08:21] Now what's the body tag. It's the very first HTML tag that you actually see in the web inspector or it's the second tag I should say because you can see the HTML but you can actually stylize the body tag and anything within that as well. So let's say we want to create a heading and add H1  like so. So we're opening and closing that and we're just going to type this is a test and we're going to save that. We're going to go to the browser and refresh this page. We can see that we have text "this is a test" now. Why did I use a H1? What does each H1 actually mean? Well, H1 stands for heading and one means that it's the first heading.

[00:09:21] Okay this doesn't mean that you can onlu have one H1 tag. You can certainly have more. Let's do this again. So underneath, we're going to have type "this as a test and this is a test again". Save that and refresh. Now we can see that we have two H1 tags.

[00:09:53] So when I say other headings, you can actually have quite a few. So if I did Heading, and then two, three, four, five, and six, Essentially H1 has more priority than H2 and that has more priority than H3 and so forth.

[00:10:15] And what I mean by priority is that it has more visually stylistically importance. The H1 is bigger than the H2 tag. The H2 tag is bigger than the H3 and so forth but it also has different meanings for things like SEO. (So search engine optimization), Where H1 is seen as a tag, which has more importance than the H2 tag.

[00:10:41] For example, you could create a blog post in WordPress where the template of that blog post has a H1 tag and the H1 tag is used as the title of the of the blog article. Whereas the H2 tag could be used for something completely different. It could be used as a way of subheading the article.

[00:11:08] So for example we could do something like this H2 and I'm actually gonna give this bit more meaning. So instead of typeing "this is a test" we're going to type "article title".

So we have an article title as the first heading and then the second heading here which is author name.

[00:12:34] Now after this we might actually want to create some paragraphs and we do that using the P tag. So we type a P tag and then we close that off and type "This is tutorial one. The basics of HTML.

[00:13:13] And can you see that we have a completely different style now because this is a paragraph and we can create several paragraphs if we wanted to. So we can copy that and paste that in.  So I wish to show you is something called bullet pointed lists.

[00:13:42] These are unordered lists which are UL and LI tags. Basically a UL is a way of that you're going to have a list and each list item is then within an LI list item.

[00:15:20] Now if we were to refresh the page here we will be able to see a bullet pointed list.

[00:15:44] The unordered list basically means that it's bulleted list. If we were to change this to be something else for example an then we woudl use an OL tag.

[00:16:08] We can see that we have one, two and three. Now we didn't actually type one, two and three. We didn't actually go one and so forth. If I was to refresh the page we'll have one that one it's just removed that it's because the browser knows that this is an ordered list.

[00:16:31] So every list item in here needs to be incremented. I'm actually going to remove, change that back to an ordered list. Now notice my browser. It breaks here.

[00:16:58] So do need to fix that and that can have a detrimental effects to other markup alongside it. So we need to change that now. As you can imagine these HTML files can get quite lengthy what tends to happen is you would create a series of HTML templates in your framework of choice which could be Symfony, Laravel.

[00:18:04] Do you follow me on Twitter. My Twitter handle is PFWD. if you've got any questions.

Thanks again. And I will see you again next time, thank you. Bye.
