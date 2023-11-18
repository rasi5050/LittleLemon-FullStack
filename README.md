# LittleLemon-FullStack
LittleLemon-FullStack Project

installation steps:
mkdir -p /home/ec2-user/rasi-projects



sudo yum install git
git clone https://github.com/rasi5050/LittleLemon-FullStack.git

sudo pip3 install virtualenv

virtualenv myprojectenv

source myprojectenv/bin/activate

sudo yum install mariadb-devel
sudo yum install gcc
sudo yum install python3-devel
pip3 install -r requirements.txt

in settings.py, add host to ALLOWED_HOSTS
python3 manage.py runserver 0.0.0.0:8000

#modify httpd configuration
cd /etc/httpd/conf.d/

#set permissions
sudo chown -R apache:apache /home/ec2-user/rasi-projects/LittleLemon-FullStack
sudo chmod -R 755 /home/ec2-user/rasi-projects/LittleLemon-FullStack

<!-- changed symlink python to python3 -->
 sudo ln -s /usr/bin/python3 /usr/bin/python


install pip3 -r requirements.txt as root user
#set secrets as env variable
ref: https://alicecampkin.medium.com/how-to-set-up-environment-variables-in-django-f3c4db78c55f
