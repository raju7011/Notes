                                                                ### MYSQL ###
   
   
   ## Mysql database settings for the django project
   
    DATABASES = {  
          'default': {  
              'ENGINE': 'django.db.backends.mysql',  
              'NAME': 'my_database',  
              'USER': 'root',  
              'PASSWORD': 'your_password',  
              'HOST': '127.0.0.1',  
              'PORT': '3306',  
              'OPTIONS': {  
                  'init_command': "SET sql_mode='STRICT_TRANS_TABLES'"  
              }  
          }  
      }  
          
1. first of all update the ubuntu system
    
        sudo apt-get update 
      
     or
      
        sudo apt update
     
2. now install the mysql in ubuntu system

        
        sudo apt install mysql-server
     
     
3. now start the service mysql

        sudo apt install mysql-server
        
4. now config mysql

        sudo mysql
        
5. change the password of the root user of mysql database

        ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
        
       
## Create database, user and grant permission to the user


1. create database in mysql

       create database raju;
       
       
       
       
2. show the list of mysql database list

       show databases;
       
    
3. Create user with the password in mysql

        CREATE USER 'raju'@'localhost' IDENTIFIED BY 'password';
        
        
        
4. Grant privileges on database to the user

    
        GRANT ALL PRIVILEGES ON database_name.* TO 'username'@'localhost';
        
        
        
        
 ## Removing the database and user from the mysql
 
 
 1. Remove the database from the mysql
 
 
        DROP DATABASES raju;
        
 2. Remove the user from the mysql


        DROP USER 'username'@'localhost';
