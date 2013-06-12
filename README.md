[OpenSprinkler-Controller](http://salbahra.github.io/OpenSprinkler-Controller)
========================

A mobile frontend for the OpenSprinkler irrigation device. Designed to allow manual control, program management (view, edit, delete and add), initiate a run-once program, view status, adjust rain delay, change OpenSprinkler settings and view logs. Screenshots available [here](http://albahra.com/journal/2013/06/opensprinkler-with-custom-web-app).

Overview:
---------

+ This application interfaces with the interval program on the OpenSprinkler which is the default software available. The application has been tested on firmware version 2.0.0 but should be compatible with 1.8.x and newer.

+ There is an authentication system in place and a guide on first run will assist in adding a new user.

+ The provided interface does not rely on the javascript files hosted by Ray therefore will work on a locally hosted server even without an internet connection. However an internet connection (with a properly configured web server and port forwarding) will allow you to access the application from anywhere.

+ For current discussion about the project please refer to the [forum post](http://rayshobby.net/phpBB3/viewtopic.php?f=2&t=154). 

Raspberry Pi Users:
-------------------

+ The application should also operate on the OpenSprinkler for Raspberry Pi so long the Raspberry Pi has the interval program installed. More information is available on  [Ray's Blog Post](http://rayshobby.net/?p=6339).

+ The application can be hosted on the Raspberry Pi itself removing any requirment for a server. You would need to install a web server and PHP on the Rasberry Pi. This can be done using the linux instructions posted below as the Raspberry Pi typically run Raspbian which is based on Debian.

Instructions:
-------------

+ You first need a working OpenSprinkler setup that you can access via a browser
  + For further information please refer to the OpenSprinkler online user manual available on [Ray's Website](http://rayshobby.net/?page_id=192)

+ Install prerequisites as needed (example for Debian using Apache web server)
  + ```apt-get install apache2 php5 libapache2-mod-php5``` 

+ Create the directory you wish to place the files in (ex. /var/www/sprinklers for http://yourwebsite/sprinklers)
  + ```mkdir -m 777 /var/www/sprinklers```

+ Download the files to your web directory using git (less steps but requires git to be installed)
  + ```git clone https://github.com/salbahra/OpenSprinkler-Controller.git /var/www/sprinklers```

+ OR download the zip file and extract the contents (more steps but also universal)
  + ```wget https://github.com/salbahra/OpenSprinkler-Controller/archive/master.zip```
  + ```unzip master.zip -d /var/www/sprinklers```
  + ```mv /var/www/sprinklers/OpenSprinkler-Controller-master/* /var/www/sprinklers/```

+ From there you may attempt to access the front end which will guide you through the rest of the install process.

[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/87d3c8783710e88024be2bf608fe8195 "githalytics.com")](http://githalytics.com/salbahra/OpenSprinkler-Controller)
