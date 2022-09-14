                                                              ## PROGRAMMING NOTES


##CREATE DATABASE IN POSTGRES

1. To enter inside the postgres database name <postgres>
  
        sudo -u postgres psql
 
2. To create database in postgres
  
        create database <database_name>;

3. Create user with encrypted password
  
        create user <username> with encrypted password <password>;

4. Grant all permission to user 
      
        grant all privileges on database kapedia to kapedia;
