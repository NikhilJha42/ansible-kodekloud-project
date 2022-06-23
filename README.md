# ansible-kodekloud-project
A repository for learning Ansible with a KodeKloud learning project.

# Bash history for manual set up
    1  clear
    2  sudo apt-get update -y
    3  sudo apt-get upgrade -y
    4  clear
    5  sudo apt-get install mariadb-server -y
    6  clear
    7  cd /etc
    8  ls
    9  cd ~
   10  clear
   11  sudo vi /etc/my.cnf
   12  clear
   13  sudo systemctl start mariadb
   14  sudo systemctl enable mariadb
   15  clear
   16  mysql
   17  sudo mysql
   18  clear
   19  cat > db-load-script.sql <<-EOF
USE ecomdb;
CREATE TABLE products (id mediumint(8) unsigned NOT NULL auto_increment,Name varchar(255) default NULL,Price varchar(255) default NULL, ImageUrl varchar(255) default NULL,PRIMARY KEY (id)) AUTO_INCREMENT=1;
INSERT INTO products (Name,Price,ImageUrl) VALUES ("Laptop","100","c-1.png"),("Drone","200","c-2.png"),("VR","300","c-3.png"),("Tablet","50","c-5.png"),("Watch","90","c-6.png"),("Phone Covers","20","c-7.png"),("Phone","80","c-8.png"),("Laptop","150","c-4.png");
EOF

   20  mysql < db-load-script.sql
   21  sudo mysql < db-load-script.sql
   22  clear
   23  sudo apt-get install httpd -y
   24  sudo apt-get install httpd php php-mysql -y
   25  sudo apt-get install apache2 -y
   26  clear
   27  sudo apt-get install php -y
   28  clear
   29  sudo apt-get install php-mysql -y
   30  clear
   31  cd /etc/httpd/conf
   32  clear
   33  cd /etc
   34  ls
   35  cd apache2
   36  clear
   37  ls
   38  cat apache2.conf
   39  clear
   40  grep 'index.html' *
   41  grep 'index.html' conf-available/*
   42  grep 'index.html' conf-enabled/*
   43  grep 'index.html' mods-available/*
   44  cd mods-available/
   45  clear
   46  ls
   47  grep 'index.html' *
   48  cd ..
   49  clear
   50  ls
   51  grep 'index.html' mods-available/*
   52  grep 'index.html' mods-enabled/*
   53  grep 'index.html' sites-enabled/*
   54  grep 'index.html' sites-available/*
   55  clear
   56  grep 'index.html' mods-available/*
   57  grep 'index.html' mods-enabled/*
   58  sudo sed -i 's/index.html/index.php/g' mods-enabled/dir.conf
   59  cat mods-enabled/dir.conf
   60  clear
   61  cd ~
   62  sudo systemctl start httpd
   63  sudo systemctl start apache2
   64  sudo systemctl enable apache2
   65  clear
   66  sudo apt-get install git -y
   67  clear
   68  git clone https://github.com/kodekloudhub/learning-app-ecommerce.git /var/www/html/
   69  cd /var/www/html
   70  ls
   71  cat index.html
   72  clear
   73  ls
   74  rm -rf index.html
   75  sudo rm -rf index.html
   76  cd ~
   77  git clone https://github.com/kodekloudhub/learning-app-ecommerce.git /var/www/html/
   78  sudo git clone https://github.com/kodekloudhub/learning-app-ecommerce.git /var/www/html/
   79  clear
   80  ls /var/www/html
   81  sudo nano /var/www/html/index.php
   82  sudo sed -i 's/172.20.1.101/localhost/g' /var/www/html/index.php
   83  curl http://localhost
   84  clear
   85  sudo nano /var/www/html/index.php
   86  sudo systemctl restart mariadb
   87  ls
   88  mysql < db-load-script.sql
   89  sudo mysql < db-load-script.sql
   90  clear
   91  ls
   92  cd /var
   93  ls
   94  cd ..
   95  cd /etc
   96  clear
   97  ls
   98  cd mysql/
   99  clear
  100  ls
  101  cd ..
  102  ls
  103  cd..
  104  cd ~
  105  clear
  106  sudo mysql
  107  clear
  108  sudo mysql
  109  clear
  110  history