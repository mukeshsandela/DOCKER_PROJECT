# DOCKER_PROJECT
Create this project after complete docker training on iice dot.

### About Project 
This project on opencart that is a online store management. Project is capabale for store management with one click.

### what is the opencart 
OpenCart is an online store management system. It is PHP-based, using a MySQL database and HTML components. Support is provided for different languages and currencies. As of May 2016, 342,000 websites were using OpenCart.

### Technology used
Docker(Containerization technology) on Red Hat Enterprise Linux 8. 

### SET-UP REQUIREMENTS
1. Docker needs to be installed on our base OS and we need to start the docker services. To start docker services permanently<br>
```systemctl enable docker```.
2. We need to install the ```docker-compose``` software inorder to use it. To install docker- compose, follow the steps: * *Go to google --> In the search box search docker compose rpm --> Choose Install ```Docker compose``` --> Based on the base OS select whether Mac, Windows or Linux etc. --> Copy the command and paste it in the terminal of the base OS.
Pull the images from docker image registry
3. Pulling MySQL Image: Use ```docker pull mysql:5.7``` to download MySQL version 5.7 image. I have used version 5.7 as it is considered the most compatible version with RHEL 8. And also Pulling ```aamservices/opencart``` Image: Use docker pull drupal:latest

```CREATING THE ENTIRE SET-UP To create the entire infrastructure, we need to write code in .yml or YAML file.```

We first create a directory where we store our yml file. Use mkdir /mycompose. We can name the directory as per our wish.
Inside ```mycompose``` directory, we create our workspace. To go inside directory, use ```cd /mycompose```.
Create the ```.yml``` file using ```vim docker-compose.yml```. docker-compose.yml is the default file where code is written. Since each compose file has same file name, it is a good practise to make seperate directory for each code.
Inside this .yml file we write our code. To start editing the text editor press i on the keyboard. After we finish writing the code, to save the file, press esc on the keyboard and type ```:w``` to save the file and ```:q``` to exit the file. To save and exit in one step, type```:wq``` together.
Inside the directory itself run the command ```docker-compose``` up to launch all the containers in the infrastructure in one go. To launch the containers in background, use ```docker-compose up -d```.
Our Opencart site is launched using MySQL as database.
To stop container, use ```docker-compose stop``` in another terminal on same directory or press left ```Ctrl + C```.
