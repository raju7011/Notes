                                                                ## DJANGO ##
   ## CREATE PROJECT ON DJANGO
   
   1. create virtual enviroment in django
   
          pip install pipenv
    
   2. activate virtual env in machine
      
          pipenv shell
   
   3. To install django in the virtual env
   
          pipenv install django==4.0.2
    
   4. To create django project (NOTE: use dot in the last for creating project in same directory)
    
          django-admin startproject <project_name> 
    
   5. To start apps in django project 
      
          python manage.py startapp <app_name>
          
   6. To create migrations files

          python manage.py makemigrations <app_name>
          
          
       6.1 To merge the migrations files

            python manage.py makemigrations --merge
          
   7. To migrate migrations file into database

          python manage.py migrate <app_name>
          
   8. To create superuser

          python manage.py createsuperuser
    
    
   9. To collect static file 
      
          python manage.py collectstatic
          
   10. To enter into the shell

            python manage.py shell
            
            
   ## FAKE IMGRATIONS AND MIGRATE
   
   1. To undo the migration 

          python manage.py migrate <app_name> zero
          
   2. To make the fake migrations

          python manage.py migrate <app_name> --fake
          
          
   ## TO FLUSH DATA BASE CONNECT TO THE PROJECT
   
   
   1. Flush database 

          python manage.py flush
          
   ## TO change the password of the superuser in django
    
    python manage.py changepassword <username/email  dependupon your models>
          
          
          
   
   

          
          
                                                                
