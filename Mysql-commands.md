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
          
  ## packget to connect mysql and django
        
    pip install mysqlclient
    
  
  ## How to install mysql in ubuntu
     
  1.Update the machine 
     
    sudo apt update
  
  2. install mysql package

    sudo apt install mysql-server
    
  3. check wether the server is running or not

    sudo systemctl start mysql.service
    
  4. check version of my sql

    mysql --version
   
  5. open mysql 

    sudo mysql
    
  6. To alter user and password

    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
    
  7. To authenticate user with pass

    mysql -u root -p
    
  8. TO create user to in mysql

    CREATE USER 'sammy'@'localhost' IDENTIFIED BY 'password';
  
  OR
    
    ALTER USER 'sammy'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
  
  9. Grant permission to user to the database

    GRANT PRIVILEGE ON database.table TO 'username'@'host';
    
  10. 
    
