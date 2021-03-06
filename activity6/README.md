# CMPSC 201 Activity 6

## Updating `progator` Docker image

If you haven't done so already during activity5, please pull the newest [progator](https://hub.docker.com/repository/docker/janyljumadinova/progator) image by running the following command:

`docker pull janyljumadinova/progator`

You can check that you have the `progator` image by running the following command and verifying that you see `progator` in the list of your Docker images:

`docker image list`

Then, run the docker container and mount your "activity6" directory as a volume by replacing `your-path/local/working/directory` in the following command with the path to your "activity6" directory:

*Mac OS*: 

`docker run -d -p 80:80 -v /your-path/local/working/directory/:/root/environment janyljumadinova/progator`

*Linux OS*: 

May need to use `sudo` as:

`sudo docker run -d -p 80:80 -v /your-path/local/working/directory/:/root/environment janyljumadinova/progator`

*Windows OS* (note the quotes in path):

`docker run -d -p 80:80 -v "C:\Users\your-path/local/working/directory/":/root/environment janyljumadinova/progator`

You can check that you have correctly started the Docker container:

`docker container list`


## Stopping the `progator` container and pruning

When you are finished working with `progator` do not forget to stop `progator` container by getting the container ID from the command you ran in your terminal:

`docker container list`

and then stopping the container by running the following command (replacing `container-ID` with the actual `progator` container ID in your terminal:

`docker container stop container-ID`

You should also remove all unused containers and images (both dangling and unreferenced) by running the following command:

`docker system prune -a`

## C and `goto` Activity

Please navigate to `activity6.md` document to learn about C programming and the tasks associated with this activity. 
 
