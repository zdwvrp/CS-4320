# Make sure: 
1. Cloned Augur
2. Have it built with `make install` ... and when in doubt: `make rebuild` (if you have an augur.config.json present it will just rebuild everything to make sure it works.)
3. Make sure you have your virtual environment activated
4. Make sure your venv is python 3 `python --version` will affirm this
5. Make sure your server can see itself: `ping 129.114.104.229` (YOUR IP, not this sample!)
6. Edit `augur.config.json` to have my external ip in place. Make "host" be the EXTERNAL IP address of your computer:
```
    "Server": {
        "cache_expire": "3600",
        "host": "0.0.0.0",
        "port": "5000",
        "workers": "4"
    },
```
7. `make rebuild`
8. `make dev`
9. (Chrome works for sure. Some version of Firebox block 'cross site calls' on these servers we are using.) Firefox error in developer console: 
```
Cross-Origin Request Blocked: The Same Origin Policy disallows reading the remote resource at http://localhost:8080/sockjs-node/info?t=1573159165913. (Reason: CORS request did not succeed).
```
10. 

## Want to start over and build augur again from scratch?
1. delete your `augur.config.json`
2. rerun `make install`


## Postgres pg_hba.conf sample that "works" ( `/etc/postgresql/11/main
` )
```
# DO NOT DISABLE!
# If you change this first entry you will need to make sure that the
# database superuser can access the database using some other method.
# Noninteractive access to all databases is required during automatic
# maintenance (custom daily cronjobs, replication, and similar tasks).
#
# Database administrative login by Unix domain socket

# TYPE  DATABASE        USER            ADDRESS                 METHOD

# "local" is for Unix domain socket connections only
local   all         postgres                peer
# TYPE  DATABASE        USER            ADDRESS                 METHOD

# "local" is for Unix domain socket connections only
local   all             all                                     md5 
# IPv4 local connections:
host    all             all             0.0.0.0/0               md5 
# IPv6 local connections:
host    all             all             ::1/128                 md5
# Allow replication connections from localhost, by a user with the
# replication privilege.
local   replication     all                                     peer
host    replication     all             127.0.0.1/32            md5
host    replication     all             ::1/128                 md5
```

## Check open ports
1. Check what ports are being used: `sudo lsof -i -P -n | grep LISTEN`
2. 


## Check if your firewall is disabled
sudo ufw status

## API Endpoints with only Five Repos
http://mudcats.augurlabs.io:5003/api/unstable/repos

## Run the Dev Server: 
`make dev`