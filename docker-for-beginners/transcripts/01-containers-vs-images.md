# Docker For Beginners
## Lesson 1
## Containers Vs Images

[00:00:00] Good morning and welcome to another [How To Code Well](https://howtocodewell.net) tutorial.

This tutorial is the first tutorial regarding Docker images and containers.

If you haven't already then do check out my Docker machine playlist - My Docker machine tutorial playlist because there's going to be some references to Docker machine commands and you might find it helpful to watch those videos first. I'll leave a link to that in the description below and at the end of this video so we're going to talk about images and we're going to talk about containers.
I think there's going to be several tutorials because there's a lot to talk about and I don't really think that I can fit everything in one. You'll fall asleep.
So for today we're just going to focus on what the differences is between an images and a container, how to get them and how to use them in a very basic manner.

[00:00:52] Okay. first I am going to talk about images. I'm not actually going to talk about containers. And the reason why is because it's like a chicken and egg scenario. You need to talk about the images first before you can talk about the containers which might seem weird because whenever everyone talks about containers or Docker they always refer to containers.

[00:01:14] It's container this and container that.  Well, actually a container needs to have an image for it to work. So you can have multiple containers that are assigned to an image.
So what is an image? Well, an image is a file I suppose, or a snapshot of a container.

[00:01:41] So a container is made from an image and you can have multiple containers from an image. The way I see it, or the very simplistic overview, I suppose is that it’s much like when you've got object orientated programming. You've got classes, class instances, and objects and so forth, where you have a class you have an instance of that class.

[00:02:02] But like polymorphism where you can have multiple classes that store multiple objects of a particular class and classes that can extend other classes. In Docker you can have images that extend other images.

Why would you have that? Well, if you're creating,  say a series of base images, you can have certain properties, certain attributes of that image that every child image would then inherit.

So for example, if you want to set up some security or some SSH rules or some  config from a very base level then you could create them in your base image. Likewise, if you wanted all your images to feed off of one particular version of Debian then you would create a base image for that.

[00:02:58] Then all your other images would extend from that base image. So there is a slight similarity. I guess it starts and stops from the terminology point of view.

[00:03:23] A Docker image can also have different properties. They can even have different volumes and different configuration that you can inject into the container. So, okay we've done a lot of talking now. Let's do some coding.

[00:03:44] Well, actually, before I do that I need to talk about where we get these images from. There's a couple of places. First is the public Docker registry. For example, Ubuntu has a repository within the Docker hub registry.

[00:04:16] The registry here is the Docker hub. Let’s bring that down so you can see [docker.com](https://docker.com) is the place to go for public and also private because you can log in here. So if I click on explore we get a whole list of repositories within this registry.

[00:04:45] Things like Nginx and busy box, you can even get the registry itself. So you can actually have private registries. For example, if you wanted to keep everything private, if you didn't want to expose parts of your infrastructure and quite rightfully so you would have a VPs perhaps that has this registry on it.

[00:05:10] And then you would use things like HTTPS and certificates to allow people in your development team or your company to access the registry the Docker login and logout protocols. You would access your own images and your own repositories from your own private registry.

[00:05:34] I'm not going to go into that too much today because there's a lot involved with setting up the private registry. All you need to know is that you can have your images in either the public domain or private domain. So going down here there's also stuff for Debian and even Mongo, MySQL, even Elastic Search. People have even set these things up for things like WordPress and Node and so forth. So it can be very application specific as well as operating system specific. So like Ubuntu and so forth. Okay, so we're actually going to pull down the Ubuntu one here.

[00:06:22] So I'm just going to click on that and we can see that this is the official repository for Ubunutu. We can see that it was last pushed nine days ago. This is obviously going to change by the time you watch this video. Let's scroll down. We can see that we've got these different tags of the Docker file. Each tag here is a version of Ubuntu. We also have a latest tag. Now the latest tag in Ubuntu sense is always the LTS version of the version of Ubuntu. If I scroll down further, we can see a little description of what Ubuntu is and then what the image does.

[00:07:06] You can see here that the Ubuntu latest, tag always points to latest LTS version which is pretty handy to know.

[00:07:28] If you've got a problem with the image, you can come here and see if there's anyone else with the same issue. Or you can do what I've done before and just say this is not working and this is what I've done. Can you help? Normally these guys, these commenters are very keen to help.

[00:07:50] So do check that out. There's also ways like IRC here that you can channel into. So we've got these tags here. We can pull down the Ubuntu image. Now I'm using the word tag and pull there's also a terms like commit and push.

[00:08:14] So you can create an image yourself and you can commit to it. You can then push that image to your private or public registry which is very handy. But what I'm going to do is just get back into the terminal because I've spoken quite a bit so let's actually write some codes and let's bring that down.

[00:08:41] So the first thing I'm going to do in this terminal is ensure that I'm running the correct Docker machine. So what I'm going to do here is just run Docker machine and then I'm just going to do active.

```
docker-machine active
```
Now this should hopefully bring back `how-to-code-well`. Yep. So we're in How To Code Well.

[00:08:59] So any image that I pull will be against this machine, which is pretty handy or assigned to this machine, which is pretty handy. So what I can do is run Docker images.
```
docker images
```
Now this is going to get the list of images that I have against this machine. We can see that we don't have any images at the moment.

[00:09:24] So this would be where the repositories are. This would be where the tags are, the image ID and so forth. The size of the file size of that image. Likewise, if I did a Docker ps -a
```
docker ps -a
```
We can see the containers that we have. Currently we have no containers at all. And that's because we have no images at all.

[00:09:42] Let's just clear that down.
```
clear
```
Let's pull down the Ubuntu image. So let's just go back to here. Let's see what we need to do. Docker pull Ubuntu. It's as simple as that. So let's do that.
```
docker pull ubuntu
```

So Docker pull Ubuntu, make sure I've spelled that right. I always spell Ubuntu wrong. So let's press enter. And what we're getting here is we're pulling down the from the latest tag because we haven't specified a tag and I'll do that in a minute just to demonstrate. It will pull down the latest by default.

So here we're pulling down all the layers that are included, all the parts that are included in this image. So now if I did Docker, whoops, Docker image we can see that we have this image that we've pulled down.

```
docker images
```

[00:10:36] We can also see that we have this one here, which is tagged none. Don't worry too much about that for this video. It just means that you can manipulate the image yourself and commit to it. And you've also got a record of what the latest one is. But let's not get into that too much.

[00:10:54] I'm also going to show you how to pull down a specific tag. So let's go back to safari, bring that back up and scroll down here. So we've got different tags that we can use. There's also a tag tab that we can just click on. And if we scroll down here theres lots and lots of tags that we can choose from which is really handy because if there's a problem, then we can sort of revert and go back to different versions and so forth.

[00:11:27] We've got the latest tag because we didn't actually specify a tag that we wanted. So we have the latest tag. Let's say I wanted to pull down 12.04. Okay. So how would you do that? Well, let's just bring that down and do Docker pull again and then it's Ubuntu.

This is the rule, the repository name and then colon. And we want to get that specific tag which is 12.04.  And we run enter on that. This is going to pull from the library Ubuntu and it's going to pull down 12.04.

```
docker pull ubuntu:12.04
```
So now what we've done is we've pulled two different versions of Ubuntu. And if I was to do Docker image
```
docker image
```

[00:12:18] We can see that we have the two images. The latest tag and the 12.04 tag. Notice again that they both have the unidentified tag that we can play with. But again i'll talk about that in future tutorials perhaps. So what I'm going to do is remove these images.

[00:12:42] I'm just going to clear the screen to give some space.
```
clear
```
Then do a Docker images again.
```
docker image
```
To remove an image what we need to do is type Docker and then it's `rim`. Okay. So `rm` removes a container `rim` removes an image. You can either specify the repository and the tag or the image ID.

```
docker rmi ubuntu:12.04
```

[00:13:07] So I will do it by image ID because it's easy to identify it.
So let's do that and we can see that we've untagged the latest and we've moved all of these things. Although the parts that made up the image, all of the layers.
```
docker rmi abcd123
```

[00:13:35] What I should do just as proof let's do Docker images.
```
docker image
```

We can see that we have just 12.04. So I know I removed 12.04 now, so let's do a Docker RMI. Now what we can do is create a list of images that you want to remove. I've already removed this.

[00:14:02] But I'm going to just paste that one in. So I'm going to remove this one. What it's going to do is it's going to complain that this image ID doesn't exist but then it's going to just remove that.

So let's just do that now so we can see that that's untagged and we can see the notice filter and move image.
```
docker rmi abc123 xyz123
```

[00:14:16] Okay. This image ID, because the image doesn't exist because I've just done that. That's a handy tip when you've got lots of images that you want to remove. Create a string of image IDs to remove and regardless of whether one has been removed or not you will remove the ones that you need.

[00:14:36] So let's clear the screen down and do Docker images and we shouldn't have any images which is good.

```
clear
docker images
```

So I'm just going to do docker pull and I'm just going to pull down the latest, so I don't need to do that. I can also do latest of course and that will pull down that latest image like so.
```
docker pull ubuntu:latest
```

Okay. So just wait for this to get. Okay. Good.

So let's do Docker images again to ensure that we have it which we do.

```
docker image
```

That's great. Again, if we did docker ps minus a.
```
docker ps -a
```

We can see that we have no containers. So this is the next part of this tutorial. How on earth do we make a container from this image?

[00:15:23] Well like I said, you can make many containers that feed off of an image. So I'll demonstrate how to create a container now.
Okay. Let's create a container from this image. And we would do that by Docker run because that's what we want to do. We want to run a container.

[00:15:48] We need to specify some flags into this, some arguments into this Docker run command.

So what I'm going to do to explain those. And I'm going to show you all the arguments that you can run with the run command.

[00:16:09] As you can see there are loads and loads and loads. We can do all sorts of crazy and wonderful things with the IP addresses, lots of stuff with the volumes, with the Mac addresses with privilege modes, with all sorts of things. The two that I'm going to use at the moment are the interactive flag, which is `-i`. This keeps the container open. This allows you to actually interact with the container which is handy and also `-t`, which deals with the TTY which is pretty handy.

So let's clear the screen down.
```
clear
```
Okay. I need to get the image ID. So Docker images and we're going to do Docker run and we're going to do `-i` and `-t`.

[00:17:03] Now we can also do just `-it` for shorthand which is pretty good. We would specify the image ID that we want to run. So I'm going to just paste that in. We're going to run it interactively and against this image ID. The thing that we want to run within the container is bin bash.
```
Docker run -it ubuntu /bin/bash
```

[00:17:28] Okay. So let's just explain what that means. So I'm going to run a container and I'm going to run it against this image and I'm going to do it interactively. By doing it interactively I've specified what command I want to run. So `bin\bash`. So running this will give me a bash shell within that container.

[00:17:54] So now notice how that's changed. So I've got a route at the container ID. Whereas the one above here is my MacBook pro command entry. So we're actually in this container that we've created. We're actually in Ubuntu. So if I was to do an `ls`, we can actually see the the file system of Ubuntu.
```
ls
```
[00:18:22] If I was to do perhaps `cat` then `etc` then get the sources list. We can actually see the sources list of Ubuntu that was used to get this image. Let's just do an exit.
```
exit
```
So this exit now is going to come out of this container. Please be aware when you're in the container because it can be a little bit confusing at times not knowing which container you're in.

[00:18:51] So let's just exit and do docker ps -a.

```
docker ps -a
```
Now this is going to list the container that we were just in. So we've created the container. That was the image ID that we used. That's the container ID that we were in. Notice that that is the same as this part here. This is the command, like I said that we were using. It was created about a minute ago and we've exited out of that container.

[00:19:15] Docker created the container a name. These names are created automatically. You can also set them up yourself. Perhaps I'll show that in a different video. We can see that this container was created and an exited. What we can do is start the container so we can do `docker start` and we can start the container against the container ID.
```
docker start containerID
```

[00:19:49] What that is going to do is it's just going to start the container. It's not going to give you that interactive shell. For example if this container was just doing a process like MySQL Apache then you would start and stop that by `docker start`

[00:20:07] As long as you've mapped the relevant bits and pieces together we can see that it's up. Now as I said before I'll show you how to do a docker start and  a Docker stop. Like so.
```
docker stop containerID
docker start containerID
```

We can also remove the container. `docker rm`. Notice we haven't added an `i` on here because we're removing the container.

```
docker rm containerID
```

[00:20:38] So we can remove that container here. And we can see that was the output. `docker ps -a` should now be empty, which it is. Okay. I'm just going to clear the screen now.

```
clear
```
Before I said earlier on that we can have many containers that are fed off of an image.

[00:19:49] I'll demonstrate that now. What I'll do is, so we've got the Docker image. I will do a Docker run. So that's gonna run the first container and notice that I've got a different container ID now because they get generated automatically.

Now let's exit out of that and then do a `docker ps -a`.

[00:21:54] So we have one container. I'm going to do `docker run` again against the image ID. Now you might think that's going to run that same container, the container that we were just in. This is not the case. If I was do `docker run`, we now get a completely different container ID. If I was to do `exit` and `docker ps -a` we can see that we actually have two containers.

[00:22:20] So these two containers are linked to the image. Like I said you can have multiple containers that are connected to the image. So you can have multiple instances of things which is pretty, pretty handy.

I'll move into more advanced features of containers and images and so forth down the line.

[00:22:45] I'm going to leave this here. This is probably enough to start with. If you've got any questions though, please let me know, put them in the comment section below. You can follow me on Twitter. My Twitter handle is [@pfwd](https://twitter.com/pfwd).  Like the video, if you've found it helpful, do share it around and do you subscribe to get the next videos coming up.

[00:23:08] Once again, thanks for watching and I shall see you again soon.

Cheers bye.