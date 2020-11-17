[00:00:00] Hello, and welcome to the third part of the HTML tutorial series. Today, we're going to look at images and how we can add an image to a web page. Now, an image tag has several attributes that we'll be discussing and going through in detail, two of which are the width and height. Now, the width and height and B.

[00:00:17] Both the percentage, as well as pixels. These are measurements of the dimensions of the image. So we can actually override the dimensions of the existing image. And we'll be talking about those in more detail as we go along the, uh, the, the other attribute that we were going to talk about. Is the source of the image.

[00:00:35] Now the image source can either be an external source. So that's an image on a separate website, somewhere else on the internet, as well as an internal source. So that's internally to the website that you're working on. So that goes through the directories. But okay. Let's uh, let's just jump into it. So the first thing I'm going to do is just copy HTML tutorial two into the third tutorial file.

[00:01:03] Let's save that. Now change a couple of bits around. So HTML tutorial, three, how to add, uh, images to web. Pages, that's fine. Oops. Spelled that wrong. Uh, let's just remove this part here. And this tutorial demonstrates how to, um, uh, embed images and, uh, a talk on image attributes. And there's going to be more attributes, um, that I won't discuss in this video because it's going to be too long.

[00:01:39] So I'm going to just do on some. Image attributes. Let's just save that. And I'm going to just go to the web browser just to ensure that this is working. That's fine. So we've got HTML tutorial, three, how to add images to web pages. This tutorial demonstrates how to embed images and a talk on some image attributes.

[00:02:01] Okay. So the first thing we're going to do now is we can add an image to this web page and we're going to. Put it in between this paragraph tag and this unordered list and to do so, we need to use the IMG tag. So I am G stands for image in HTML. So let's go here. That's in between the paragraph and the unordered list.

[00:02:23] And we do, I M G like, so now the image tag is a self-closing tag, which means we can do backslash. And then the closing tag symbol let's save that. Now, obviously we haven't actually added the source of the image here. So if I was to refresh this page, now it will look exactly the same, but there's a little bit of gap ready for the image to be added.

[00:02:47] Okay. So the first thing we need to do is we need to, um, add an attribute that represents the source of the image. And like I said, this can be an external source or this can be an internal source for now, though. We're just going to focus on an internal image. To this website. Now I have an image, um, called, uh, logo dot PNG.

[00:03:08] Now that is in the current working directory of this tutorial. So this tutorial file tutorial three dot HTML is in the same directory as this logo dot PNG. Now that's very important. And I'll talk about that in a minute. Let's just close this far now and to reference the source, we use something called SRC.

[00:03:28] So that's the attribute name, SRC, and we can equal that. Two B logo dot P N G. Let's save this now and go back into the browser and refresh the page. And we can see that we have this logo. Now, this image that has been added, um, now, um, As you can see it's, it's conforming to the original image dimension. So that's the original height and width of this image, um, which, uh, goes from there to here and then down, like, so, but we can change this on the fly in the HTML so we can actually expand and stretch this image if we need to.

[00:04:11] Um, let's do that now. Let's change the image width. So width. Is equal to, and I'm going to remove this. I'm going to scale this down to be 200. So that's 200 pixels. Let's save this, go back into the browser, refresh the page. We can see that it's now, um, constrained to 200 pixels in width. Notice the height has changed because we haven't defined the height, the height.

[00:04:39] Ratio gets automatically calculated based on its width. Likewise, if we were to change the height, but not the width, it would do the same. So let's change that to be height and save that. Um, I'm going to change that to be a hundred instead, just to. Be a little bit more adventurous. Let's [00:05:00] refresh the page and we can see that the width has also changed because we've conformed.

[00:05:04] We've, we've enforced that the height is set to a hundred and therefore the width dimension gets changed to in the same ratio as the original image. But we can do something a little bit crazy. We can actually change both the width and the height and stretch and, uh, crop the, or not crop stretch and, um, um, uh, Uh, compact the image, um, on the flight as well.

[00:05:30] Let's do that. So height of a hundred, I'm going to do width of, um, if I spell that correctly, that'd be great width of I'm going to do, um, uh, 500, like, so refresh the page. And we can see that we've stretched this image out. It's now 500 pixels, but we're keeping, we're enforcing the height to be 100 and we can, we can do it the other way.

[00:05:56] So, um, we can do height of 10 for instance and width actually. No, I'll do width of 10. Oops, the Heights of, uh, of 300, let's save that and refresh the page. And as you can see, we've completely distorted this image. Now this image is totally unreadable, but it's conforming to the rules that we've put into the image tag.

[00:06:23] So regardless that the image itself has, um, a set dimensions, the HTML has overridden those dimensions. Um, and likewise, we can change this to be instead of pixels, we can use percentages. So let's do, um, width here of hundred percent. Whoops, like, so I'm just going to put height of 200 safe that refresh the page and we can see that it's now spanning to be the whole width of the page.

[00:06:55] Um, and we're forcing the height as well. Let's just, um, Remove those, put them back to the original. So in fact, I'm just going to do a width is 200, because that will move the height. To be the correct height too, with like, so let's just refresh to bring it back to where it was. Okay. So another thing that we can do is, um, like I said before, we can change the source.

[00:07:25] So it referenced an external file. Let's do that now. So, what I'm going to do is just go to, uh, my blog and I'm going to take this image here. So what I'm going to do is just open up the development developer tools, which is somewhere on here. Um, show web inspector. There we go. And, um, you might not be able to see this, cause this is awful for the page.

[00:07:54] Let's just, uh, detach that. So you can see what I'm doing a little bit better. So, um, what I need is this image here. And if I do, um, uh, Edit that the attribute I can now copy this attribute. So that's the SRC tag that we've had added, uh, in the previous tutorial. If I copied that, um, closed this down, going back to this tutorial, let's just move that a little bit this way so you can see it.

[00:08:24] Um, what I can do is change that to be whoops. And paste that in. So that's actually referencing a external image. That's the Gravatar image that I've got. Let's save this and go into here and refresh this page and you can see that we've now changed the image to be this external image. It's a bit blurry.

[00:08:48] So what I'm going to do is just change the width to be 96. I think that's probably the best width let's save that, refresh the page. And we can see that it's changed  the width to be at 96. Which makes it look a little bit more clearer. I'm going to just remove the width. So it conforms to its original height and width.

[00:09:10] I think it is 96 anyway. Yeah, it is. Okay. So the next thing we're going to do is also add at what's called an alt tag. Now an alt tag is used by search engines, um, to, uh, find the alternative texts. So in some cases where the image doesn't actually load, perhaps it's your linking to an external image and the image.

[00:09:31] Gets removed then this, um, piece of text is the alternative representation of the image is also used in things like screen readers as well. Um, So it has an accessibility benefit too. Also, this is, like I said, it's used by search engines, so it has a very good SEO impact as well to your website. Um, so for example, if you've got a website that is full of images, maybe it's a portfolio website, maybe it's an art website and you want.

[00:10:00] Uh, uh, demonstrating where you're showing off your, your, uh, your art, your images, um, then, or it could be even a product category catalog. Um, then do add some alt tags because they are picked up by, uh, uh, search engines as well. Let's do this now. So let's change or let's add an old attack to this. So alt is equal to, and we're just going to do Peter Fisher.

[00:10:30] Let's save that. Now this is not actually going to do anything on the, on the F at the moment, because we have the image, um, that's that's already in place. So if I was to save that refresh the page, then nothing has actually changed because the image has been found. However, um, what we can do is what I can do is demonstrate a failing image.

[00:10:54] So let's say this is sort of gravatar.com, which.com dot um,  X, because it's not going to work now, that image is not going to work because the source is totally broken. I've just put a dot X in front of the.com, which doesn't exist. Let's see if that's refresh the page and notice it's got this, um, question Mark symbol in like, so, but if I was to view the source of this, um, this page, And have a look at that section here.

[00:11:28] We can see that it has this alt tag now in certain browsers. Um, this will this word, this, uh, this alt tag will be shown instead of this, um, this, uh, question Mark, um, which is useful for, like I said, with screen readers. And it will also be picked up by, uh, image searches as well. So the, the SEO crawling the bots will be looking for the old tags too.

[00:11:55] Let's however though, put it back to how it was. And all the way back to the start. So logo dot on, save that, refresh the page. Okay. So that is a quick tutorial on HTML images, how to add images, a discussion on the source. External sources and internal sources, as well as changing the dimensions, the height and the width using percentages as well as pixels and a brief explanation to alt tanks, why to use them and how to use them.

[00:12:28] Okay. If you found this tutorial helpful, then please do give it a thumbs up. If you've got any comments or questions or queries. Do you put them in the comment section below and I will get back to you as soon as I can, um, subscribe to get the next tutorials coming along as well as the web chats I do every week.

[00:12:43] Thanks again for watching and I shall see you again soon. Thank you. Bye.