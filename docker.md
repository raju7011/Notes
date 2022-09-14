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
                - POSTGRES_DB=${DB_NAME}
                - POSTGRES_USER=${DB_USER}
                - POSTGRES_PASSWORD=${DB_PASSWORD}

            <django_service_name>:
              restart: always
              container_name: <conatiner_name>
              image: kapedia
              build: . # location where to build docker images
              volumes:
                - .:/<volume_name>
              ports:
                - "8000:8000"
              depends_on:
                - < serive_name_on_which_it_depend>
              env_file:
                - <name_of_env file>

          # For volumes
          volumes:
            static:
            
   5. To build the docker-compose image and run the container

          sudo docker-compose up
   
   6. To enter into the docker containder shell

          sudo docker exec -it <container_id> bash
