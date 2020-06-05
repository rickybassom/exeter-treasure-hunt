# exeter-treasure-hunt (ExePlore)

An interactive location based treasure hunting game designed for freshers at the Streatham Campus (University of Exeter).

<img src="https://camo.githubusercontent.com/e3beb78904c249e43c1042997977f738e9be6af8/68747470733a2f2f692e696d6775722e636f6d2f4c4c63413777792e706e67" data-canonical-src="https://camo.githubusercontent.com/e3beb78904c249e43c1042997977f738e9be6af8/68747470733a2f2f692e696d6775722e636f6d2f4c4c63413777792e706e67" width="220" height="400"/> ---- 
<img src="https://camo.githubusercontent.com/f530779679407cb648300eea929ee74c0daff79a/68747470733a2f2f692e696d6775722e636f6d2f7a7950473066652e706e67" data-canonical-src="https://camo.githubusercontent.com/f530779679407cb648300eea929ee74c0daff79a/68747470733a2f2f692e696d6775722e636f6d2f7a7950473066652e706e67" width="220" height="400" /> ---- 
<img src="https://camo.githubusercontent.com/7014da1048d1d9ac21c1e8247498fd85b2d2a24c/68747470733a2f2f692e696d6775722e636f6d2f6c5865714770772e706e67" data-canonical-src="https://camo.githubusercontent.com/7014da1048d1d9ac21c1e8247498fd85b2d2a24c/68747470733a2f2f692e696d6775722e636f6d2f6c5865714770772e706e67" width="220"  height="400" />

![](https://i.imgur.com/M4ochgql.png)

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
