# PersonalExpenseTracker
#Exp12
exports.handler = function(event, context, callback){
  console.log("Incoming Event:",event);
  const bucket = event.Records[0].s3.bucket.name;
  const filename = decodeURIComponent(event.Records[0].s3.object.key.replace(/\+/g,' '));
  const message = `An Image is Added - ${bucket} -> ${filename}`;
  console.log(message);
  callback(null, message);
};
#Exp11
import json
def lambda_handler(event,context);
first_num = 100
second_num = 200
sum = first_num+second_num
return num

#Exp9
 sudo apt-get update 
manjusha@apsit:~$ sudo apt-get install wget build-essential unzip openssl libssl- dev 
manjusha@apsit:~$ sudo apt-get install apache2 php libapache2-mod-php php-gd libgd-dev 
manjusha@apsit:~$ sudo adduser nagios
manjusha@apsit:~$sudo groupadd nagcmd  
manjusha@apsit:~$sudo usermod -a -G nagcmd nagios  
manjusha@apsit:~$sudo usermod -a -G nagcmd www-data
manjusha@apsit:~$cd /opt/ 
manjusha@apsit:~$sudo wget https://assets.nagios.com/downloads/nagioscore/releases/nagios
4.4.3.tar.gz  
manjusha@apsit:~$sudo tar xzf nagios-4.4.3.tar.gz
manjusha@apsit:~$cd nagios-4.4.3 
manjusha@apsit:~$sudo ./configure --with-command-group=nagcmd  
manjusha@apsit:~$sudo make all 
manjusha@apsit:~$sudo make install  
manjusha@apsit:~$sudo make install-init  
manjusha@apsit:~$sudo make install-daemoninit  
manjusha@apsit:~$sudo make install-config  
manjusha@apsit:~$sudo make install-commandmode  
manjusha@apsit:~$sudo make install-exfoliation
manjusha@apsit:~$sudo cp -R contrib/eventhandlers/ /usr/local/nagios/libexec/ 
manjusha@apsit:~$sudo chown -R nagios:nagios/usr/local/nagios/libexec/eventhandlers
manjusha@apsit:~$sudo nano /etc/apache2/conf-available/nagios.conf 
Add below lines to nagios.conf file. 
ScriptAlias /nagios/cgi-bin "/usr/local/nagios/sbin" 
<Directory "/usr/local/nagios/sbin"> Options ExecCGI 
AllowOverride None 
Order allow,deny Allow from all 
AuthName "Restricted Area" AuthType Basic 
AuthUserFile /usr/local/nagios/etc/htpasswd.users Require valid-user 
</Directory> 
Alias /nagios "/usr/local/nagios/share" 
<Directory "/usr/local/nagios/share"> Options None 
AllowOverride None Order allow,deny Allow from all 
AuthName "Restricted Area" AuthType Basic 
AuthUserFile /usr/local/nagios/etc/htpasswd.users Require valid-user 
</Directory>

install using following commands. 
manjusha@apsit:~$cd /opt 
manjusha@apsit:~$sudo wget http://www.nagios-plugins.org/download/nagios-plugins- 2.2.1.tar.gz 
manjusha@apsit:~$sudo tar xzf nagios-plugins-2.2.1.tar.gz manjusha@apsit:~$cd nagios-plugins2.2.1 
Now compile and install Nagios plugins 
manjusha@apsit:~$sudo ./configure --with-openssl 
manjusha@apsit:~$sudo make  
manjusha@apsit:~$sudo make install --with-nagios-user=nagios --with-nagios- group=nagios
manjusha@apsit:~$sudo htpasswd -c /usr/local/nagios/etc/htpasswd.users nagiosadmin
manjusha@apsit:~$/usr/local/nagios/bin/nagios -v /usr/local/nagios/etc/nagios.cfg  
manjusha@apsit:~$ sudo service nagios start 
Step 7 – Access Nagios Web Interface 
Access your nagios setup by access nagios server using hostname or ip address followed by /nagios. 
http://127.0.0.1/nagios/ 
Prompting for Apache Authentication Password – 
username: nagiosadmin 
Password : 123456 (which you enter while configuration)







