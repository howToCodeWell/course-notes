# Dock For Beginners #2 Making changes to images

[00:00:00] Hello, welcome to another. How to code? Well, YouTube tutorial. My name is Peter Fisher and this is the 
second part of the Docker image, Docker container, a set of tutorials in this tutorial, I'm going to focus on how we can
change a minute plate, a Docker image. Once we have the image downloaded to the machine in the previous tutorial, in the
intro tutorial.

[00:00:22] A discussion on what the differences between a Docker image and what the difference is between a container
and the things that defined the two as well as a brief tutorial, I suppose, a demonstration of how to pull down an image
and how to run them as containers or run containers from the images.

[00:00:42] I highly recommend you check that video out. The previous one because it will give you some insight and some
better knowledge for this video. Also I've got a Docker machines tutorial, uh, that I recommend you, you watch too, if
you haven't already done. So I'll put links to those in the description and the YouTube cards up here, uh, as I go along.

[00:01:06] But, uh, today we're just going to focus on how we can minute a plate, these images once we have them. 
So I'm going to ensure that I'm in the right machine. So let's just do Docker and machine active, and this should return
the how to code well machine, which it does. And if we did Docker images, we shouldn't have anything here.

[00:01:25] And if we did Docker, PS minus a, we shouldn't have anything there. So you can see I've got nothing up my
sleeve. So let's just clear this down. And what I'm going to do is stop. Uh, Paul, and we're just going to get
the, you burn to the latest you want to image. So this is, this step is exactly what we did in the previous video.

[00:01:48] Uh, obviously I have more exp explanation as to what I was doing, uh, but we'll just wait until this gets in 
store. Okay. So if we did Docker images we can get the image ID. All right. So what we need to do is create a container
from this image first, before, you know, in order to manipulate this image, we might.

[00:02:10] Get a container. Then we, uh, create this container and, uh, get into it using a bash shell. Then we install
some bits and pieces. And then what we need to do is save though those bits and pieces to the image so we can use it
again. So the first thing we do is Docker run and minus it. Uh, we've got the image ID here and we're going to go
in as been.

[00:02:36] Being bashed. So this again will, uh, bin bash. This will take me into a, a shell, which it does. And what I
can do is do an app get updates. So that's going to update the sources.

[00:02:55] And I'm going to install NPM. So if we go, ah, yes. So this is actually creating changes to the image. Okay. 
This is creating changes to the image on this Docker machine.

[00:03:19] And as this is running through, I would like to just explain that, uh, there are things called Docker files. 
Now a Docker file is, um, what, what is used to actually create the images from scratch. 
I will go into those in more detail, uh, in future videos and how to correct Docker files and so forth. But the point 
I want to make is that it's what I'm doing now is on, uh, I'm kind of changing.

[00:03:46] I'm changing the image without changing a Docker file, which in some cases is okay. Especially if I'm
committing it back to a registry, but it's always good. If you want to start from scratch these changes to have the
install NPM command within the Docker file as well. So then you can put that into source control and other developers 
can use it, but anyway, I digress.

[00:04:14] So let's do NPM minus V and we can see here that we've got 3.5 0.2. That's fine. And I'm just going to exit 
out of this container. Okay. So, um, obviously if I did Docker images, If I was to remove this image and then do a pull 
from Ubuntu. Again, I won't have the NPM because this is something that I've added myself.

[00:04:38] So what I need to do is commit to this image, um, and I'm committing it to, to my, uh, local health code
well machine. So what I do is do Docker commit, uh, In fact, actually I need to do Docker PS. My a cause, you know
I said before that container is a snapshot of an image. So we need to do DACA commit minus no we don't Docker commit and
then the com the container ID.

[00:05:10] So it's that one there, and we need to give it a name as well. So I'm going to, do you been to. Been to
and I'm just going to put a dash N P M hyphen NPM. So what van is going to do after I press enter is it's actually going
to create another image or a snapshot of that container with NPM, uh, in there.

[00:05:34] And if I was, uh, working against a private or a public public Docker registry in which I could log into, I
could then do a Docker push and push this, uh, or Docker tag target, and then put it. So if I now did Docker images, we
can see that we have a third image here. You been to hyphen NPL. So that was the first one that we got, the latest that
we got.

[00:06:00] And then this is the one that we have literally just created. So let's do a Docker PS minus a.
I'm just going to clear the screen, uh, Docker, PS, minus a, and. So we've got that container that we were just in 
I'm going to do a Docker RM, um, and remove it because what I want to do is do a Docker images and I want to do a Docker
run minus i t.

[00:06:31] And I'm going to use a, I'm going to use this image, the new image that we've got. And I'm going to run that.
And actually what I'm going to do is just run NPM minus fee. Okay. So that will print out the version of NPM from the
container. So if I did that, we should get 3.5 0.2, which we do now, if I was to do that against the previous image
the image that we first got from the public registry, the Ubuntu repository.

[00:07:03] So find it NPS. If I run that against here we will get an error and we'll get an error because NPM isn't 
installed in that image. It is in this image, but not in that image. So if I did that, then we get an error a pretty 
nasty one. And basically that means that the executable far can not be found in the path.

[00:07:26] Um, so I'm just going to click. That down. Um, and you took up, he S minus a and likewise, if I was to let's 
just do a Docker RM, there are other ways of actually getting into these containers using Docker exe, but I will show
that to you later on. I'm going to just kill that and also kill that one.

[00:07:53] Uh, like, so, so Docker, PS, mines, ain't got nothing there to go back to Docker images. So if we were to do
a Docker run minus i t to the original image ID, so that's the original Ubuntu image. And then if I was to just run that
as bin bash, And did a NPM minus V. We can see that is c'mon. It cannot be found.

[00:08:26] So I'm going to exit out of you I'm going to now jump into being bash in this image and. Paste that in and do
an NPM minus feet and we can see it is there. So this is how you create your images, where you update your images and
you commit them. And like I said, if you, if you were connected or locked into a registry, you could then do a tag and
a push to push this stuff up.

[00:08:57] It's very important to keep committing as you go. Also, like I said, it's very important to have a Docker
file that you can update as you go to, just to keep a record of what you've done. I'm going to leave it there, even
though there's a lot more to, uh, to this subject, I'll probably pick that up again in the following tutorials, but if
you've got any questions, then please do let me know, put them in the comments section below like the video, if you
found it helpful and please do share it around, subscribe to get the next set of tutorials and also the web chats that
I do every week.

[00:09:31] So thanks again for watching and I shall see you again soon. Bye.

