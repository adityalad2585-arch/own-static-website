# my facebook- website 

## introduction

### This project is a simple demo of a *Facebook clone web page* created using basic HTML .It is not the real Facebook, but just a practice project to learn and understand how to build web pages with styling, text, and images.The project displays a *facebook message* along with the *Facebook logo*, giving a look similar to the original site.

##  Features  
- Simple HTML structure for easy understanding  
- Styled text with headings and welcome message  
- Facebook logo image added to the page  
-  Clean and minimal design  
-  Beginner-friendly project for practicing web development  

## prerequisites
- active aws account 
- A running linux Ec2 instance
- SSH access with facebook.pem
- Basic knowledge of Linux commands
- Nginx installed on the server
- Project files (HTML) ready to upload
- Security Group with port (81) open
- website will be accessible at
- http://18.234.117.81

##
## steps for deployment


![My Image](Screenshot2%20(12).png)

##
### step 1 :  connect to ec2 instance using SSH key
    
### 1.copy the SSh key

##


![My Image](Screenshot%20(29).png)
##
### 2. go to SSh key folder and open git bash and paste the command

##

![my image ](Screenshot%20(30).png)
### step2: install nginx web server

* sudo yum update 


![my image ](Screenshot2%20(3).png)

##
### install nginx web server

* sudo yum update nginx -y
##
![my image ](Screenshot2%20(4).png)




##
### step 3: start enable and check status of the web server
*  sudo systemctl start nginx
* sudo systemctl  enable nginx
* sudo systemctl status nginx
##
![my-image](Screenshot2%20(5).png)
##
## step 4. go to the default directory (/usr/share/nginx/html/)
* cd//usr/share/nginx/html/
![my-image](Screenshot2%20(6).png)



## step 5. create directory(facebook) and go inside that directory
* sudo mkdir facebook 

![my-image](Screenshot2%20(7).png)


## step 6 . download the image to be insert in the website
* image download for index page

##

![my-image](Screenshot2%20(9).png)
##
## step 7 . create index.html page
* sudo vim index.html

* insert code in index.html 
##

![my-image](Screenshot%20(32).png)
##
## step 8. configuring nginx root directory
* sudo vim /etc/nginx/nginx.conf



![my-image](Screenshot%20(33).png)
##
* find the server and change the root directory and restart nginx
* sudo systemctl restart  nginx



##
## step 9. go to security groups and add rule on port no 81 and save it

##

![my-image](Screenshot%20(35).png)


##

![my-image](Screenshot%20(31).png)
##
## step 10. copy public IP and paste to any browser
##

![my-image](Screenshot%20(34).png)

##
## step 11. see your website on browser
##

![my-image](Screenshot%20(37).png)



##

## summary

Install Nginx, place your website files in the web directory, set proper file permissions test the configuration, restart Nginx, allow web traffic through the firewall, and optionally secure the site with SSL using Let’s Encrypt.
##
