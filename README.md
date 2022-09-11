# TWN_Module_7_Docker_for_local_dev


#Docker for local development

#In this branch I will use Dockerfile for nodejs application and to build a docker image.
#I will use the server.js and app directory I got form TWN git lab to connecto to my Docker mongodb container and run mongo express as a UI for the database


#Notes on contents of Dockerfile

# From - always the first line of a Dockerfile and dictates the basis this container is starting from. For example in this exersise if I just specified 13-alpine which is just a linux distribution it woould not have node installed. However node:13-alpine specifies that you are running node from the 13-alpine distribution

#Env- this can define the enviroment varibles you would like to include in the container. 
#in this docker file I will be defining the user to be admin and the password to be password


#Run - runs commands inside the container, the command this time will create a directory for the app files

#Copy - this command takes the first argument as where to copy a file from the host machine and the second dictates where in the container to copy to

CMD - multipe run commands from an entry point
