################################################################################
THIS PROGRAM SETUP A NODE.JS CODE INSIDE A DOCKER CONTAINER
###############################################################################
The based images runs upon a Node image of version 15.
A dockerfile was used to build the image file
An /app directory was created inside the WORKDIR
The package.json file was first copied in to /app dirctory since docker image build execute in a layered approach
Then followed by RUN command that installs npm.
The COPY command is used to copy all dependencies into the the /app directory and EXPOSE command maps the local port
in this case 3000 to the running container.
The CMD command is use at run time to start the node.js components.

It is worth noting that the container when running is attached to a volume to make the state persitent, such that any change on
our code is refelected in the front end. In this case, the nodemon restarts the flow whenever there is a change.

One last thing. the .dockerignore file is used to stop docker from copying unncessary files inside the container ducring the build image
run time.



*******************THANK YOU*********************************************************

