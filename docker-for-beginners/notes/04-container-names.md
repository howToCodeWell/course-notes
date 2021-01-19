---
course_slug: docker-for-beginners
tutorial_number: 4
type: note
---

A Docker container is named randomly when it is created. 
This name can be set using the `--name` argument when running the container.

To create a Nginx container with a name of `webapp` run the following command
`docker run -d --name webapp nginx`

Docker commands that normally require the container id can now use the container name.
