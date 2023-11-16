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

