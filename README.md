# TWN_Module_7_Docker_for_local_dev

In this branch I will use Docker Compose to run multiple containers

My Docker compose file is called mongo.yaml and there I have defined that I want to start mongodb from my local host using port 27017 connecting to port 27017. I am setting with an enviroment varible that the user will be admin and the password will be password. In the same network I would like to start mongo-express service using port 8080 for the host and 8081 for the remote.
