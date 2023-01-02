# Hosting Full Stack Application

This application is provided from Udacity to be hosted into AWS with CircleCI.

# Getting Started

1- Clone this project locally.
2- Open a the project and follow the instructions in the installation step.
3- you need to create .env file follow the instructions in the Variables Environment step.
4- you need to create set_env file follow the instructions in the Variables set_env.sh file step.

The project can run but is missing some information to connect to the database and storage service. These will be setup during the course of the project

# Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```


# Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres. <Place holder for link to classroom article>
1. In AWS, provision a s3 bucket for hosting the uploaded files. <Place holder for tlink to classroom article>
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.



# Variables Environment 

If you want to run the Udagram-Api locally, create .env file in Udagram-api directory and add the below variables.

```bash
PORT= 3000
PORT_DB= 5432
POSTGRES_HOST= localhost
POSTGRES_DB= Database_Name
POSTGRES_USERNAME= Database_Username
POSTGRES_PASSWORD= Database_Password
URL = http://localhost
JWT_SECRET  = Any_String
AWS_REGION = us-east-1
AWS_PROFILE = default
AWS_BUCKET  = Bucket_Name
AWS_ACCESS_KEY_ID = YOUR_AWS_IAM_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY=  YOUR_AWS_IAM_SECRET_ACCESS_KEY
```



# set_env.sh file
Make sure you have set_env.sh file in udagram directory.
The file contains the following:

```bash
# This file is used for convenience of local development.
# DO NOT STORE YOUR CREDENTIALS INTO GIT
export POSTGRES_USERNAME=postgres
export POSTGRES_PASSWORD=myPassword
export POSTGRES_HOST=mydbinstance.csxbuclmtj3c.us-east-1.rds.amazonaws.com
export POSTGRES_DB=postgres
export AWS_BUCKET=arn:aws:s3:::myawsbucket-75139724085
export AWS_REGION=us-east-1
export AWS_PROFILE=default
export JWT_SECRET=mysecretstring
export URL= Your backend url that hosted on EBS
export AWS_ACCESS_KEY_ID = YOUR_AWS_IAM_ACCESS_KEY_ID
export AWS_SECRET_ACCESS_KEY=  YOUR_AWS_IAM_SECRET_ACCESS_KEY
```


# Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

# Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

# License

[License](LICENSE.txt)
