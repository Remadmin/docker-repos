## whuwxl/pptpd

A simple docker container running pptp vpn server.

### Installation

    docker pull whuwxl/pptpd:latest

### Simple Usage

Demonstration ONLY!
Username: username
Password: password

    docker run --name pptpd --privileged -d -p 1723:1723 whuwxl/pptpd

### Custom Users and Passwords

Write custom username and password to a plain file and mount to pptpd container when run container. You can replace 'myname' to your username and replace 'mypass' to your password.

    echo "myname * mypass *" >> /chap-secrets
    docker run --privileged -d -p 1723:1723 -v /chap-secrets:/etc/ppp/chap-secrets:ro --name pptp pptp