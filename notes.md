                                                        ## PROGRAMMING NOTES ##

INSTALLL POSTGRE IN UBUNTU MANCHINE

1. update the machine

        sudo apt update
        
2. install postgresh package along with contrib

        sudo apt install postgresql postgresql-contrib
        
4. ensure that service is stared

          sudo apt install postgresql postgresql-contrib
         
5. check the version of psql to ensure it's working

          psql --version

CREATE DATABASE IN POSTGRES

1. To enter inside the postgres database name <postgres>
  
        sudo -u postgres psql
 
2. To create database in postgres
  
        create database <database_name>;

3. Create user with encrypted password
  
        create user <username> with encrypted password '<password>';

4. Grant all permission to user 
      
        grant all privileges on database kapedia to kapedia;
 
5. If we have to change the password for the user
      
       ALTER USER <user_name> WITH PASSWORD '<new_password>';
  
6. If we have to drop the database
  
       DROP DATABASE <database_name>;

 7. If we have to drop the user
  
        DROP USER <user_name>;
