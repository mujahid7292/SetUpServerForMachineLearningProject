# We have to provide a base image name. Depending upon this 
# base image our new docker image will be created. So write:
FROM ubuntu:18.04
# Put this newly created image maintainer name & 
# emaill address.
MAINTAINER Saifullah Al Mujahid <mujahid7292@gmail.com>
# Now run some command to build this image:
RUN apt-get update
# Now we will install or upgrade python3
RUN apt-get update && apt-get install -qq -y python3.7
# We will install python3 pip
RUN apt-get update && apt-get install -qq -y python3-pip
# Now we will install flask inside the container
RUN pip3 install --no-cache-dir -qq flask
# Now we will create a folder `app` inside docker image and
WORKDIR /app
# Here workdir command is same as cd
# Now we will copy everything from Docker_Flask directory of our 
# local computer to docker image app directory. As now we are
# currently in this Docker_Flask directory so we will put only .
COPY . /app
# As flask development server use port 5000
# So we will open port 5000 inside docker container.
EXPOSE 5000
# Now we will run our flsk app
ENTRYPOINT ["python3"]
CMD ["run.py"]
