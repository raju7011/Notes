                                                                ## DJANGO ##
   ## CREATE PROJECT ON DJANGO
   0. Install pipenv in your machine
    
          pip install pipenv
   
   1. create virtual enviroment in django
   
          pipenv --python3.10
    
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
  
  11. TO run the local server

            python manage.py runserver
            
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
    
   ## To enter inside the project database shell
   
    python manage.py dbshell
    
   ## To check either the migrations is excuted or not
   
    python manage.py showmigrations
    
   ## django-extension
  
   1. To rest dajngo db (drop and recreate)
   
    python manage.py reset_db
    
   2. TO generate Er diram of the all django models

    python manage.py graph_models -a -o myapp_models.png
          
          
          
   
   

          
          
                                                                
