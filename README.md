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

<img width="1920" height="976" alt="Screenshot2 (12)" src="https://github.com/user-attachments/assets/917e1fe8-b51e-463f-b3d1-d669e1d989b2" />


##
### step 1 :  connect to ec2 instance using SSH key
    
### 1.copy the SSh key

##

<img width="1904" height="861" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/cb817873-bdf8-476a-978f-db1485dac145" />

##
### 2. go to SSh key folder and open git bash and paste the command

##
<img width="1914" height="1019" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/b413f864-5f9a-48b5-ad93-ff5e1f3f3ddf" />

### step2: install nginx web server

* sudo yum update 

<img width="1918" height="1031" alt="Screenshot2 (3)" src="https://github.com/user-attachments/assets/a795a048-0036-4dd6-b3f1-a15f9c39053c" />

##
### install nginx web server

* sudo yum update nginx -y
##
<img width="1918" height="1027" alt="Screenshot2 (4)" src="https://github.com/user-attachments/assets/6716d466-40e8-4871-980f-1c0b26778b32" />





##
### step 3: start enable and check status of the web server
*  sudo systemctl start nginx
* sudo systemctl  enable nginx
* sudo systemctl status nginx
##

<img width="1920" height="1021" alt="Screenshot2 (5)" src="https://github.com/user-attachments/assets/9f2a2fd5-6f4d-42a5-af51-e93945974f79" />

##
## step 4. go to the default directory (/usr/share/nginx/html/)
* cd//usr/share/nginx/html/ *
<img width="1920" height="1015" alt="Screenshot2 (6)" src="https://github.com/user-attachments/assets/9b4d285e-c699-43b1-9f23-d2aa6f65c803" />




## step 5. create directory(facebook) and go inside that directory
* sudo mkdir facebook


<img width="1920" height="1015" alt="Screenshot2 (7)" src="https://github.com/user-attachments/assets/23a4ea02-ccd5-4129-96f7-fd1a6ec2415e" />


## step 6 . download the image to be insert in the website
* image download for index page

##

<img width="1916" height="1017" alt="Screenshot2 (9)" src="https://github.com/user-attachments/assets/837fe9ac-aa58-476f-8479-ce112371a9ab" />

##
## step 7 . create index.html page
* sudo vim index.html

* insert code in index.html 
##
<img width="1920" height="1031" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/58ceea5c-c92d-4c79-8554-a4874fc86221" />

##
## step 8. configuring nginx root directory
* sudo vim /etc/nginx/nginx.conf


<img width="1920" height="1017" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/9275047b-6e68-4ed5-a866-fff47c4ea16f" />

##
* find the server and change the root directory and restart nginx
* sudo systemctl restart  nginx



##
## step 9. go to security groups and add rule on port no 81 and save it

##

<img width="1920" height="919" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/085a9cb3-f82c-49bc-8918-4225cb187905" />

##
<img width="1920" height="1024" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/5a1598ef-193e-4ec4-a9fe-bbb8b507ca50" />


##
## step 10. copy public IP and paste to any browser
##

<img width="1919" height="992" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/767fe216-49a8-4dcd-9324-7446fdd50478" />


##
## step 11. see your website on browser
##


<img width="1920" height="973" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/4ce11228-6b0c-4c75-ba7b-5d301141e96f" />



##

## summary

Install Nginx, place your website files in the web directory, set proper file permissions test the configuration, restart Nginx, allow web traffic through the firewall, and optionally secure the site with SSL using Let’s Encrypt.
##
