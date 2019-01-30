---
title: "Geonode Install using Docker"
date: "2018-12-25"
description: "Geonode Install using Docker "
disable_comments: false # Optional, disable Disqus comments if true
authorbox: true # Optional, enable authorbox for specific post
toc: false # Optional, enable Table of Contents for specific post
mathjax: true # Optional, enable MathJax for specific post
categories:
  - "Cheetsheets"
tags:
  - "Cheetsheets"
---
Geonode Installation on Docker using shell scripts 
<!--more-->
## Geonode Install using Docker


      # Geonode Docker Installation Script, to run use following commands
      # cd shellscripts
      # sh geonode.sh
      # provide public ip address when asked


      # Once installation is complete check at IP address
      # Use 'screen' command to run the server again using following command
      # cd geonode
      # screen
      # docker-compose -f docker-compose.yml -f docker-compose.override.localhost.yml up
      # Use CTRL + A and d to dettach from the server
      # now you can exit without shutting down the server

      cd ~

      sudo apt-get update

      sudo apt install -y screen

      sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common

      curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

      sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

      sudo apt-get update

      sudo apt-get install -y docker-ce

      sudo usermod -aG docker $USER

      source $HOME/.bashrc

      docker run hello-world

      sudo curl -L https://github.com/docker/compose/releases/download/1.19.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

      sudo chmod +x /usr/local/bin/docker-compose

      git clone https://github.com/GeoNode/geonode.git

      cd geonode

      echo "Enter Your Public Address or enter localhost if your are using on local machine"
      read IPADDRESS

      # Replace localhost ALLOWED_HOSTS=['localhost', ] to ALLOWED_HOSTS=['*' ]
      sed -i "s/'localhost',/\'*\'/g" docker-compose.override.localhost.yml

      sed -i "s/localhost/$IPADDRESS/g" docker-compose.override.localhost.yml

      docker-compose -f docker-compose.yml -f docker-compose.override.localhost.yml up --build

Following script git url : https://github.com/tayyabsayyad/shellscripts/blob/master/geonode.sh

    {{<youtube NT0YUUM34F0>}}
