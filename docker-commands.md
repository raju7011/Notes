                                                                  ### DOCKER ##
  ## TO COMPOSE DOCKERFILE
  
  1. Create docker file

          touch Dockerfile
          
  2. Code for the docker file 

          FROM python:3.8

          ENV PYTHONUNBUFFERED=1

          WORKDIR /<work_dir_name>

          RUN apt-get update

          COPY requirements.txt .


          RUN pip install -r requirements.txt

          COPY . .

          COPY ./entrypoint.sh /

          ENTRYPOINT ["sh","/entrypoint.sh"]

          EXPOSE 8000
          
  3. To create docker-compose.yml

          touch docker-compose.yml
          
  4. Code for docker-compose.yml

          version: '3.3'

          services:

            <db_service_name>:
              image: < db_image_name>
              
              restart: always
              
              container_name: <conatiner_name>
              
              environment:
                - POSTGRES_DB=${NAME}
                - POSTGRES_USER=${USER}
                - POSTGRES_PASSWORD=${PASSWORD}

            <django_service_name>:
            
              restart: always
              
              container_name: <conatiner_name>
              
              image: <image_name>
              
              build: . # location where to build docker images
              
              volumes:
                - .:/<volume_name>
                - 
              ports:
                - "8000:8000"
                - 
              depends_on:
                - < serive_name_on_which_it_depend>
                - 
              env_file:
                - <name_of_env file>

          # For volumes
          volumes:
            static:
            
   5. To build the docker-compose image and run the container

          sudo docker-compose up
   
   6. To enter into the docker containder shell

          sudo docker exec -it <container_id> bash
          
   7. To stop the docker container

          sudo docker-compose down
          
   8. To see the list of running docker containers

          sudo docker ps
          
   9. To see all the docker containers

          sudo docker ps -a
   
   10. To delete docker container

            sudo docker rm <container_id>
            
   11. To see the list of docker images

            sudo docker images
            
   12. To delete docker images

            sudo docker rmi < image_id>
            
   13. prune all images, or manually delete one by ID
    
            docker image prune -a
            docker image rm <image_id>
            
   14. Pruning Containers And Volumes
        Docker never removes containers or volumes (unless you run containers with the --rm flag), as doing so could lose your data. However, you may             have old data backed up that needs to be garbage collected.
        Much like images, Docker provides a prune command for containers and volumes:
        
            docker container prune
          
            docker volume prune

          
    
