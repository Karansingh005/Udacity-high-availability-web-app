# Udacity-high-availability-web-app
This is a repository, conatining cloudformation scripts to deploy a highly available web application on Amazon Web Services platform. This repository was made, as a part of my Nanodegree project with Udacity. 

## Architecture Diagram
The architecture diagram has been provided in the repository, in the name of [WebApp.jpeg](https://github.com/Karansingh005/Udacity-high-availability-web-app/blob/master/WebApp.jpeg). I used a Website, named [Lucid.com](http://www.lucidchart.com/) to design my own Achitecture diagram.

## Requirements to run the scripts on your local machine
Here are some of the requirements, to run these scripts on your local machine:
1. Download a text editor like Microsoft Visual Studio Code. Link to download Microsoft Visual Studio Code: https://code.visualstudio.com/
2. Set up an Amazon Web Services account. Here's link to create your AWS account: https://portal.aws.amazon.com/billing/signup#/start
3. Set AWS Command Line Interface on your device. Download AWS CLI tool using the link: https://aws.amazon.com/cli/.
4. Use the following command in your command prompt or terminal of your VS Code to set-up your AWS account.
`$ aws configure`
5. Follow the steps to create Access Key and Secret Access Key in IAM, using the following link: https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html#cli-quick-configuration

## Commands to run the Cloud Formation scripts
1. Downlaod [Create command file](https://github.com/Karansingh005/nd9991-c2-Infrastructure-as-Code-v1/blob/master/supporting_material/create.sh) and [Update command file](https://github.com/Karansingh005/nd9991-c2-Infrastructure-as-Code-v1/blob/master/supporting_material/update.sh) into the same working directory, as the CloudFormation Scripts.
2. Make sure that, the present working directory of your VS Code terminal, be same as the directory, where scripts are present. 
3. Now, to depoy/create the cloud formation stack, write command: `$ ./create.sh <name-of-the-stack> <name-of-the-template-flie-in-yml> <name-of-the-parameters-file-in-json>`
4. Make sure, to first deply [WebApp-Network.yml](https://github.com/Karansingh005/Udacity-high-availability-web-app/blob/master/WebApp-Network.yml) infrastruture, before deploying [WebApp.yml](https://github.com/Karansingh005/Udacity-high-availability-web-app/blob/master/WebApp.yml) scripts. And make sure to run [WebApp-Network-Paramters.json](https://github.com/Karansingh005/Udacity-high-availability-web-app/blob/master/WebApp-Network-Parameters.json) with WebApp-Network.yml and [WebApp-Paramters.json](https://github.com/Karansingh005/Udacity-high-availability-web-app/blob/master/WebApp-Parameters.json) with WebApp.yml.
5. To update the created stack, run the following command: `$ ./update.sh <name-of-the-stack> <name-of-the-template-flie-in-yml> <name-of-the-parameters-file-in-json>`
6. You can check AWS console, and go AWS Cloud Fomation to check if your cloud formation stack has been deployed, or not.
7. If the stack dosen't get deployed, check the logs of CloudFormation stack, to check for the error in script.

Link to website: http://webap-webap-1dv4b250l3nc6-1257434246.us-west-2.elb.amazonaws.com/ (The link will not work now, since I've taken down the stack after the review of my project, to avaid extra costs)
