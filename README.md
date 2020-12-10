# Deep-Learning-Docker-image


###########################################  
Run using docker for the first time  
###########################################  

#docker pull waleedka/modern-deep-learning
docker pull ufoym/deepo:cpu
docker images
docker images -a


docker run -d -it <image_id>
docker ps
docker ps -a

-----------------------------------------
## now you can open as many terminals and run the following
-----------------------------------------

docker exec -it <container_id> bash





###########################################  
Save a checkpoint by commiting  
###########################################  
exit
docker ps -a
docker commit <container_id> new_image_name:tag_name(optional)



###########################################  
Docker exit the running detached container  
###########################################  
docker ps -a
docker stop <container_id>



###########################################  
Run using docker the previously exited container  
###########################################  
docker ps -a
docker start <container_id>
-----------------------------------------
## now you can open as many terminals and run the following
-----------------------------------------

docker exec -it <container_id> bash





###########################################  
Load a previous docker commit in detached mode/ in background mode  
###########################################  
docker images
docker run -d -it new_image_name:tag_name
-----------------------------------------
## now you can open as many terminals and run the following
-----------------------------------------

docker exec -it <container_id> bash


###########################################  
Copy model weights to/from docker container  
###########################################  
docker cp <host_directory> <container_id>:<container_path>

docker cp /root/FYP_Model_weights/ f4a08fba2d31:/root/
docker cp f4a08fba2d31:/root/ /root/FYP_Model_weights/
