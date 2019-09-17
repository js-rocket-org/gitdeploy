This folder contains script files used for deployment of source code through git

ssh keys can be generated with the command:

ssh-keygen -t rsa -b 4096 -C "some_comment_or_email" -f ./id_rsa -N ""

Create a folder for each project containing these 5 files:
altssh      - the ssh wrapper containing pointer to custom ssh key
altgit      - the git wrapper that uses the ssh wrapper above
id_rsa      - the ssh private key file to access your project
id_rsa.pub  - the ssh public key file to access your project
known_hosts - the known hosts file for your project repository server

Then use a script to call the altgit command to update your repository.
The type of script will depend on the webserver you run.
There is example scripts for PHP and nodejs in this repository

