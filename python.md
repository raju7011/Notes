                               install python and changes the version of python
                               
1. first of all update your machine

        sudo apt-get update
        
      or
        
       sudo apt update

2.  Install prerequisite package

        sudo apt install software-properties-common
        

3. After fulfilling all of the prerequisites, move ahead and add the “deadsnakes” PPA to your system source list

        sudo add-apt-repository ppa:deadsnakes/ppa
     

4. Install python of your choices here is the example of python 3.10

        sudo apt-get install python3.10
        
       
5. check the python version

        python --version
        
6. Finally you can choose multipal python version

       sudo update-alternatives --config python
       
7. python  and python3 same

        sudo apt-get install python-is-python3

       
