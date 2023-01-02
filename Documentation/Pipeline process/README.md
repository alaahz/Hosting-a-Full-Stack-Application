
# Pipeline process

## Pipeline process Diagram
![Pipeline  Diagram](https://i.ibb.co/0fmW1Cp/Pipeline-process-Diagram.png)


1- The developers’ teams update the code, commit the changes, and push to the GitHub repository.

2-	The GitHub account must be connected to CircleCi account and Circleci follows the project and set the environment variables.

Note: To add environment variables, click on project settings > environment variables > add environment variables.

3-	GitHub repository triggers the CircleCI.

4-	The CirecleCI reads the .circleci/config.yml to perform the jobs that will run the scripts from package.json to install, build, and deploy the frontend and backend.

5-	The AWS will upload the frontend to S3 and backend to EBS and S3. 

