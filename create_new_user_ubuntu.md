# Create new user in Ubuntu and add ssh key <br/>

**command to run after installing ubuntu or creating new droplet in digital ocean** <br/>
sudo apt update <br/>
sudo apt dist-upgrade <br/>

**command to create new user** <br/>
adduser username <br/>
usermod -aG sudo username <br/>


**to change user** <br/>
su - username <br/>

**add authorized key to user** <br/>

**create public-private key for server that will create all folders** <br/>
ssh-keygen <br/>

**add your public key into authorized_keys** <br/>
nano ~/.ssh/authorized_keys  <br/>
copy public key and save <br/>

chmod -R go= ~/.ssh <br/>
chown -R $USER:$USER ~/.ssh <br/>

