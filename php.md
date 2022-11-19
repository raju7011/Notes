### COMMAND TO INSTALL PHP IN UBUNTU 

1. UPDATE AND UPGRADE UBUNTU MANCHINE

        sudo apt install software-properties-common ca-certificates lsb-release apt-transport-https
   
2. INSTALL FEW PHP IN THE MACHINE

        sudo apt install software-properties-common ca-certificates lsb-release apt-transport-https
       
        LC_ALL=C.UTF-8 add-apt-repository ppa:ondrej/php
 
3. AGAIN THE UPDATE THE MACHINE

        sudo apt update
       
4. INSTALL PHP IN THE MACHINE AS VERSION YOU REQURIED

       sudo apt install php8.1 

5. IF YOU REQURIED EXTENSION FOR PHP

        sudo apt install php8.1-[extension]
     
6. EXTENSTION YOU WANT TO INSTALL

        sudo apt install php8.1-mysql php8.1-mbstring php8.1-xml php8.1-curl
        
 7. FINALLY CHECK THE PHP VERSION

        php --version
