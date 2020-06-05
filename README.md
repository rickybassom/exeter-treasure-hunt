# exeter-treasure-hunt (ExePlore)

An interactive location based treasure hunting game for the Streatham Campus (University of Exeter)

## Link to design
https://github.com/rickybas/exeter-treasure-hunt/wiki/Design

## Link to users manual
https://github.com/rickybas/exeter-treasure-hunt/wiki/Users-Manual

## Setup
Clone repo:

`git clone https://github.com/rickybas/exeter-treasure-hunt.git`

`cd exeter-treasure-hunt`

Install dependencies (make sure [system dependencies](#system-dependencies) are installed before this):

`pip3 install -r requirements.txt`

Set up MySQL database, enter password for user root@localhost:

`mysql -u root -p < app/db/init.sql`

Then populate the database with initial hashed and salted passwords and usernames, enter password for user root@localhost

`python3 app/db/populate_users_database.py`

`python3 app/db/populate_user_cards_database.py`


## Running Locally

`python3 app/wsgi.py`

*optionally use -p to enter password for user root@localhost*

## Run tests

`python3 app/test_http_reqs.py`

`python3 app/test_db.py`

## Or run using docker

```
docker build -t eth . 
docker run -p 5000:5000 eth
```

## System dependencies
* Python 3.7
* MySQL 5.7
* docker and docker-compose
