# LittleLemon Restaurant - FullStack Project

I have deployed the project on AWS, view at https://bit.ly/LittleLemon

## Motivation:
This is my modified capstone project for [Meta Back-End Developer Certification](https://www.coursera.org/account/accomplishments/professional-cert/QPWERYDG5685) where I developed a full-stack website for restaurant management.

<img width="1800" alt="Screenshot 2023-11-18 at 14 08 17" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/2ca3b828-2a00-4662-97f8-aeacd84f196d">

## What all have I done?

● Developed a full-stack website for restaurant management with user-friendly interface with HTML, CSS, and JavaScript and Django partials ensuring a responsive and engaging user experience.

● Utilized Django Modelforms, Generics to build robust back-end functionalities, including menu display, table reservation system and live updates of reservation details.

● Implemented interactive UI components for users to  easily book reservations, select preferred dining times, and view availability and prevent duplicate reservations using REST API’s, DOM manipulation and localstorage.

● Deployed and configured application on AWS Cloud leveraging EC2 and RDS(MySQL); Oversaw the security aspects by isolating sensitive data as environment variables, setting up security groups and VPC in AWS.

## Whats used?

Python, Django, HTML, CSS, JavaScript, AWS EC2, RDS(MySQL)

## Functionality

Website features homepage for restaurant, menu display, make reservations, view all reservations, get directions and about page.

## How to run?

`$ mkdir LittleLemon-FullStack`

`$ cd LittleLemon-FullStack`

`$ pip3 install virtualenv`

`$ virtualenv myprojectenv`

`$ source myprojectenv/bin/activate`

`$ git clone https://github.com/rasi5050/LittleLemon-FullStack.git`

`$ cd LittleLemon-FullStack`

----------------------------------------------------------------------------
create .env file

`$ vi littlelemon/.env`

paste below configuration with your values, refer for [setting up env variables](https://alicecampkin.medium.com/how-to-set-up-environment-variables-in-django-f3c4db78c55f), [create django secret key](https://djecrety.ir/)

### Note: these values will work for you, but recommended to replace with your values

```
SECRET_KEY=1*sf%cpjo7sst6n@%l-le0@+*v_z8uff2in051@mc-auc^9z4m
DATABASE_NAME=reservations
DATABASE_USER=db_user
DATABASE_PASS=strongPass349f*(
DATABASE_HOST=localhost
```
save file using :wq!

----------------------------------------------------------------------------

`$ brew install mysql`

refer [create mysql database, user and password](https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql)

login to mysql

`$ mysql -u root -p`

`$ create database reservations`

`$ CREATE USER 'db_user'@'localhost' IDENTIFIED BY 'strongPass349f*(';`

`$ GRANT PRIVILEGE ON reservations.* TO 'db_user'@'localhost';`

exit mysql

---------------------------------------------------------------------------
Note: install if required, these packages were required for AWS EC2 linux 2

`$ sudo yum install gcc`

`$ sudo yum install python3-devel`

---------------------------------------------------------------------------

`$ pip3 install -r requirements.txt`

`$ python3 manage.py createsuperuser`

provide username, email, password of your choice

`$ python3 manage.py makemigrations`

`$ python3 manage.py migrate`

`$ python3 manage.py runserver 8000`

Navigate your browser to http://127.0.0.1:8000/. That's it!

### Add menu items

go to http://127.0.0.1:8000/admin

login with superuser credentials created before

<img width="1800" alt="Screenshot 2023-11-18 at 15 20 14" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/f3c1fd29-b012-4d58-9e1c-dfb9f96bfdb3">


go to Menus -> ADD MENU

add title, price and description. Place an image with <title>.jpg at <project-folder>/restaurant/static/img/<title>.jpg





## Functionality:

### Homepage for restaurant

<img width="1800" alt="Screenshot 2023-11-18 at 15 18 06" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/d2fbd539-fd39-46fa-9fdb-1ea7b3c54640">

### Menu view

Displays menu items list and detailed page on clicking with images. Images are mapped from <project-folder>/restaurant/static/img/<title>.jpg, where <title> is the title added for the Menu item using Django admin

<img width="1799" alt="Screenshot 2023-11-18 at 15 18 47" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/4f44bb46-4d6d-4321-8d7a-bbd6964313b0">

<img width="1800" alt="Screenshot 2023-11-18 at 15 20 53" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/4db28b13-eca6-420f-af11-127da0ee21ca">

### Reserve a table

<img width="1800" alt="Screenshot 2023-11-18 at 15 22 56" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/285eae1b-7dd0-4465-ae4e-742b5d417b70">


date picker and shows existing bookings for the selected date
<img width="1394" alt="Screenshot 2023-11-18 at 15 23 32" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/6309bad8-d7bf-4bdf-8e17-f0b5af08ac51">

available time slots
<img width="1405" alt="Screenshot 2023-11-18 at 15 23 40" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/aa038bf6-af9a-4a2b-a864-e8d240792e19">

### View all reservations

<img width="1800" alt="Screenshot 2023-11-18 at 15 26 17" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/13caf186-8ec3-4b0f-b3d0-a02db92eb163">

### Get directions

<img width="1799" alt="Screenshot 2023-11-18 at 15 26 47" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/1a027209-fe9c-42fa-99b2-e4a72870733d">

### About page

<img width="1798" alt="Screenshot 2023-11-18 at 15 27 19" src="https://github.com/rasi5050/LittleLemon-FullStack/assets/12760472/0142aa46-a341-4b28-9a8d-79d9725a4f1f">

--

Let me know what you feel about this project. Happy to connect on [Linkedin](https://www.linkedin.com/in/rasi5050/)

Happy learning!

rasi01@syr.edu

