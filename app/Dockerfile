# set base image (host OS)
FROM ubuntu:20.04

# install python
RUN sudo apt install python3.8
RUN sudo apt install python3-pip

# set the working directory in the container
WORKDIR /code

# copy the dependencies file to the working directory
COPY requirements.txt .

# install dependencies
RUN pip3 install -r requirements.txt

# copy the content of the local src directory to the working directory
COPY src/ .

# command to run on container start
CMD [ "python", "./server.py" ]