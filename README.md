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


#By following through this exersise I have demonstrated the role of what a continous intergration tool like jenkins would perform in the pipeline 

#A development server would then run a docker compose file starting the docker images sourced from docker hub as well as the one from your private repository




#Docker Volumes


#Volumes are required when dealing with persisting data in Docker. As all the date without volumes is being stored in a virtual file system in the container any data will be lost once the conatainer is lost or restarted

#There are 3 different volume types



#Volume type 1: Host Volume

#docker run -v /home/mount/data:/var/lib/mysql/data
                 ^host path      ^virtual file system path

#The host volume is where you define both the path for the host file system and virtual file system



#Volume type 2: Anonymous Volumes

#docker run -v /var/lib/mysql/data
                ^just the virtual file system path is defined



#Volume type 3: Named Volumes

#docker run -v name:/var/lib/mysql/data
              ^the name on host   ^virtual file system path

#Here you can reference the volume just by name on the host file system. This is the method that should be used in productions.
