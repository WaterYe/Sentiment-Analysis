# Sentiment-Analysis
CMU 14848 Cloud Infrastructure Extra Project

For video recording of code walkthrough and demo, please visit https://www.youtube.com/watch?v=PDu1HBFeYn8

## Step 1 Build Container Images

SA - Frontend

![build-frontend](https://i.imgur.com/NuiSah1.jpg)

SA - Webapp

![build-webapp](https://i.imgur.com/WZTiAhy.jpg)

SA - Logic

![build-logic](https://i.imgur.com/HrPEOff.jpg)

## Step 2 Push Images to Docker Hub

SA - Frontend

![push-frontend](https://i.imgur.com/ubtDOuL.jpg)

SA - Webapp

![push-webapp](https://i.imgur.com/KhOocOu.jpg)

SA - Logic

![push-logic](https://i.imgur.com/yXfHfib.jpg)

Docker Hub Screenshots

### Docker Hub URLs

![hub](https://i.imgur.com/YULOXmI.jpg)

SA - Frontend
https://hub.docker.com/repository/docker/waterye/sentiment-analysis-frontend

SA - Webapp
https://hub.docker.com/repository/docker/waterye/sentiment-analysis-web-app

SA - Logic
https://hub.docker.com/repository/docker/waterye/sentiment-analysis-logic

## Step 3 Deploy Docker Images to GCP

### Pull images from Docker Hub and tag
Screenshot of images in Cloud Shell

![pull-and-tag](https://i.imgur.com/5ukE5K1.jpg)

### Push to GCR

![gcr-push-image](https://i.imgur.com/SaeAblB.jpg)

Screenshot of GCR

![gcr](https://i.imgur.com/9MZMUmk.jpg)

## Step 4 Create Kubernetes Cluster

![create-cluster](https://i.imgur.com/KcyOjc1.jpg)

## Step 5 Create containers for each mircoservice on GKE

### SA - Logic

Create Deployment

![pods](https://i.imgur.com/mpqTp12.jpg)

Modify yaml config file to expose port 5000

![yaml](https://i.imgur.com/AMOZhtF.jpg)

Create Service

![service](https://i.imgur.com/PANCjvR.jpg)

Verify Flask application With Postman

![post](https://i.imgur.com/jShwg2u.jpg)

### SA - Webapp

Create Deployment

![pods](https://i.imgur.com/QVtIDwE.jpg)
![deployment](https://i.imgur.com/uU08NDz.jpg)

Modify yaml config file to expose port 5000

![yaml](https://i.imgur.com/621wWj5.jpg)

Create Service

Verify Spring application with Postman

![post](https://i.imgur.com/vAY3Gjq.jpg)

### SA - Frontend

Create Deployment

![pods](https://i.imgur.com/ayZHCQo.jpg)

![deploy](https://i.imgur.com/Omg0dYF.jpg)

Create Service

![service](https://i.imgur.com/zqAD0cj.jpg)

## Screenshot of Application

![Capture](https://i.imgur.com/HLKj5NR.jpg)