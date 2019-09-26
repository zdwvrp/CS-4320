# Project 4: Deployment Focus (team)
1. Create an ssh key and share the public key with Dr. Goggins. https://confluence.atlassian.com/bitbucketserver/creating-ssh-keys-776639788.html **caution** : If you already have an ssh key that you use to login to servers, you can reuse the public version of that key. You do NOT, in that case, need to create a new one!
2. You will get access to individual instances in an email from Dr. Goggins on your university email account on Friday, presuming you have sent the public key to him. You will get your server emailed either way, but you will not be able to access it until you send Dr. Goggins your public ssh key. 
3. Login to the computer using the instructions provided. 
4. Create a python virtual environment for this project on your new server. 
```
virtualenv --python=python3 project4
```
You should see something like: 
    Already using interpreter /usr/bin/python3
    Using base prefix '/usr'
    New python executable in /home/sgoggins/project4/bin/python3
    Also creating executable in /home/sgoggins/project4/bin/python
    Installing setuptools, pkg_resources, pip, wheel...done.
5. Activate your virtual environment `source project4/bin/activate`
6. Clone Augur: git clone https://github.com/chaoss/augur.git
7. Checkout the `class-demo` branch: 
    - `cd augur/`
    - `git checkout class-demo`
8. Create your postgres database
```
    sudo -u postgres psql
    postgres=# create database augur;
    postgres=# create user augur with encrypted password 'mypass';
    postgres=# grant all privileges on database augur to augur;

```
9. Exit the Postgres interface and return to be your user. 
```
postgres-# \q
postgres@js-104-101:~$ exit
logout
(project4) sgoggins@js-104-101:~/augur$ 

```
10. Install NodeJS: `sudo apt-get install nodejs`
11. Install Node Package Manager: `sudo apt-get install npm`
11. Install and compile augur by doing a `make install`
    - When prompted, create all the workers, EXCEPT, do NOT install the "value worker". 
```
        Installing repo_info_worker
        Would you like to install value_worker?
        1) y
        2) n
```
    - When prompted, install at command line
    - When prompted, install frontend dependencies
12. Have these steps completed before class on Tuesday, October 1. If you have installation or setup issues, submit them to the Slack Channel. 

