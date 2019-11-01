# My first Individual python project
An application where people can come up and get decent ideas on what book to readand the user can post their own reviews on a book. 
The user can post review update and delete their posts. It has been mainly built in python language using Flask webframework. 

# Prerequisite 
  1. Make sure the very first thing you do is __"sudo apt-get update"__
  2. Make sure you have __python3__ installed on your VM
  3. Install __pip3__
  4. Clone this repository to your machine
  
# Running the App in different ways

 ## On the Local Machine
  1. cd in the Flask_APP
  2. type __"pip3 install -r requirements.txt"__
  3. use __"python3 run.py"__ to run the app
  
 ## Making Jenkins run it
  1. Add a user calling it pythonadm this can be done using the code "__sudo useradd -a -s /bin/bash pythonadm__"
  2. Make sure you check beforehand whether or not python3 and pythonadm has permission to access the documents or not. If there is        no permission granted, this can be done by writing the code and entering the file by "sudo visudo" and further input: 
    
    __jenkins ALL=(ALL:ALL) NOPASSWD:ALL__
    __pythonadm ALL=(ALL:ALL) NOPASSWD:ALL__
  
 ## Using Docker
  1. Docker can be uploaded to your machine using __curl https://get.docker.com | sudo bash__
  2. Once its installed you can run using the code, to build an image, __docker build -t flask-app .__
  3. Next step after writing the code above to run it is __docker run -d -p 5000:5000 flask-app__
