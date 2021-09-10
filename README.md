# lambda-puppeteer

lambda-puppeteer is a node lambda function that uses puppeteer to scrape html. The included serverless config containerizes it, publishes an image to ECR, and deploys a lambda function using it.

This repo is a POC for deploying containerized nodejs lambda functions out of ECR with the serverless framework.

## Building and deploying the app locally:

Login Docker to AWS ECR:

> aws ecr get-login-password --region \<region> | docker login --username AWS --password-stdin \<account>.dkr.ecr.\<region>.amazonaws.com

Create serverless application and update the org:

> serverless

Deploy to lambda:

> serverless deploy

## Example output:

![facebook.com Test](/docs/facebook_test.png)