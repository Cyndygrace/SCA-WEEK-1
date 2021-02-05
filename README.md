# SCA-WEEK-1

Task covers the following topic: Cloud vm, Creating users, groups &amp; giving permissions

# QUESTIONS From Mentor

1. add me as user on your VM (on any cloud of your Digital Ocean, GCP, AWS, Azure, ..). My pub key file will be attached here
2. Write a brief on DevOps in not more than 250 characters
3. copy the file to your Cloud VM
4. Create a group called SCASchool
5. Add me to that group
6. Change the group owner of the file in #2 to SCASchool
7. Give write permission on the file to the SCASchool group

# Commands to execute the following steps

1. I created a virtual machine on google cloud platform with SSH Key
2. I ssh into the vm using - ssh External IP
3. To add mentor as a user:- sudo useradd -m username
   sudo passwd username
4. To add mentor public key:-
   a. cd .ssh
   b. ll
   c. vim authorise_keys
   d. i
   e. add mentor public key
   f. esc
   g. :wq
5. To write biefly on DevOps in a file on vm:- vim dev-summary.txt
6. To create a group:- sudo groupadd groupname
7. To add mentor to the group:- sudo usermod -a -G groupname username
8. To change the group owner of the file in #5 to SCASchool:- chgrp groupname filename
9. To give write permission on the file to the SCASchool group:- chmod g+w filename

# QUESTIONS From SCA

1. Create 3 groups and 15 users
2. Assign the 15 users across the 3 groups
3. Demonstrate that user(s) in a group cannot access files/folders that belong to another group unless they are added to that group

# Commands to execute the following steps

1. To create a group:- sudo groupadd groupname
2. To add a user:- sudo useradd -m username
   sudo passwd username
3. To assign user to group:- sudo usermod -a -G groupname username
4. Verify user cannot access file in another group:- su username
   cat filename
