## Install NodeJs

https://nodejs.org/en/download/

To check if it is install properly execute the follow commands in terminal window 
```
npm -v
node -v
```
## Install Docker

https://docs.docker.com/desktop/mac/install/

To check:
```
docker --version
docker-compose --version
```
## Install Git

https://git-scm.com/download/win)

To check:
```
git --version
```
## Clone repository

```
git clone git@github.com:nancy134/user-service.git
```
## Add .env file

In the user-service directory add a file called .env which the following contents:

(Get the values over Slack as these cannot be checked into the repository)
```
DATABASE_URL=
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=
AWS_SQS_NEW_USER_QUEUE=
AWS_SNS_UPDATE_USER_TOPIC=
```
## Run docker image
```
docker-compose build
docker-compose up
```
## run npm install to get tool
```
npm install
npx sequelize db:migrate
```
## Check if it is running properly

Put the following in the browser:

http://localhost:49161/

You should get back "user-service"
