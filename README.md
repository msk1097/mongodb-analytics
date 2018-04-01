# coursera
#### https://www.coursera.org/learn/introduction-mongodb
#### https://www.coursera.org/learn/introduction-mongodb/supplement/OwBDM/setting-up-your-course-environment

## set up conda environment
#### >> conda create --name intro-to-mongodb
#### activate the environment
#### >> activate intro-to-mongodb
#### then install
#### >> conda install python=3.6
#### >> pip install pymongo dnspython

## set up git hub repository
#### C:\dev\code\mongodb-analytics
#### with the folder structure
####     └── intro-to-mongodb
####        ├── mflix
####        └── notebooks

## install mongodb enterprise
#### https://www.mongodb.com/download-center#enterprise
#### shell is here:
#### C:\Program Files\MongoDB\Server\3.6\bin\mongo.exe
#### database server is here:
#### C:\Program Files\MongoDB\Server\3.6\bin\mongod.exe
#### add this location to 'system environment variable' PATH 
#### apply to 'system' not 'user' path variable and make it highest priority
#### so copy this: C:\Program Files\MongoDB\Server\3.6\bin;
#### test my running at the command prompts
#### >> mongo --nodb
#### >> quit()

## set up atlas
#### https://www.mongodb.com/cloud/atlas
#### login: peternorton99@yahoo.com.au
#### cluster name: mflix
#### cluster user: analytics
#### cluster password: analytics-password

## import data into atlas (movies_initial.csv)
#### template
#### >>mongoimport --type csv --headerline --db mflix --collection movies_initial --host "<CLUSTER>/<SEED_LIST>" --authenticationDatabase admin --ssl --username analytics --password analytics-password --file movies_initial.csv
#### with parameters
#### >>mongoimport --type csv --headerline --db mflix --collection movies_initial --host "mflix-shard-0/mflix-shard-00-00-heksn.mongodb.net:27017,mflix-shard-00-01-heksn.mongodb.net:27017,mflix-shard-00-02-heksn.mongodb.net:27017" --authenticationDatabase admin --ssl --username analytics --password analytics-password --file movies_initial.csv

## set up compass
#### https://www.mongodb.com/download-center?jmp=nav#compass
#### go to atlas and get the connection string
#### go back to compass and connect to host

## start jupyter notebook
#### from this folder
#### C:\dev\code\mongodb-analytics\intro-to-mongodb\notebooks
#### start a jupyter notebook server
#### >> jupyter notebook
#### then interact with notebook here
#### http://localhost:8888/
#### if folder isnt visible then specify as follows (use double quotes)
#### jupyter notebook --notebook-dir "C:\dev\code\mongodb-analytics\intro-to-mongodb\notebooks"

