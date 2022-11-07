# TWN_Module_7_Docker_for_local_dev


#Docker for private repository


# When pulling from Docker hub you can perform a command like 

#Docker pull reddis 

#and because you are using Docker hub it knows which container and version to pull the image from. However when using a private repository this is not the case

#so once you have authenticated your docker account with aws the first command you will need to push is

#docker tag my-app:1.0 895154248152.dkr.ecr.us-west-2.amazonaws.com/my-app:1.0

#To break this down this command is basically creating a associating version 1.0 of my-app on your local machine with version tag 1.0 of the remote my-app located at


#895154248152.dkr.ecr.us-west-2.amazonaws.com/my-app

#After this you simply need to perform the docker push command referencing the remote repo exactly as well as the tag

#If you want to make changes to the docker file or other files in the image rebuild the docker image with a new tag and then push this new tagged version to the remote repo



