# Fire Detection Using YOLOV5

## Web application preview

<img src="https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/d6467dd6-19c3-4ae4-acdd-cbe5a6472e9e" width="1050" height="550">

## Sample output on Images

<!-- ![val_batch2_labels_1](https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/ab75fb21-cad2-420a-aeb8-28f491931378)
![val_batch2_labels_2](https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/2ca04141-3fa7-48df-9496-7e2857cf933c)
![val_batch2_pred_1](https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/2cc488c7-98f0-4f9c-82a1-c23178a216de)
![val_batch2_pred_2](https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/6cc15df9-4afc-40ca-a77b-1e48caefbe9b) -->

| <img src="https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/ab75fb21-cad2-420a-aeb8-28f491931378" width="300" height="200"> | <img src="https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/2ca04141-3fa7-48df-9496-7e2857cf933c)" width="300" height="200"> |
| :------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/2cc488c7-98f0-4f9c-82a1-c23178a216de" width="300" height="200"> | <img src="https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/6cc15df9-4afc-40ca-a77b-1e48caefbe9b" width="300" height="200">  |

## Sample output on Video

![fire](https://github.com/Msparihar/Fire-Detection-using-YoloV5/assets/75237981/84fc40f8-f87e-4962-b0ef-c454cd341842)

## Steps to use this repository.

### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n fire python=3.7 -y
```

```bash
conda activate fire
```

### STEP 02- install the requirements

```bash
pip install -r requirements.txt
```

### STEP 03- run the app locally

```bash
python app.py
```

Now,

```bash
open up you local host and port
```

# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

    #with specific access

    1. EC2 access : It is virtual machine

    2. ECR: Elastic Container registry to save your docker image in aws


    #Description: About the deployment

    1. Build docker image of the source code

    2. Push your docker image to ECR

    3. Launch Your EC2

    4. Pull Your image from ECR in EC2

    5. Lauch your docker image in EC2

    #Policy:

    1. AmazonEC2ContainerRegistryFullAccess

    2. AmazonEC2FullAccess

## 3. Create ECR repo to store/save docker image

    - Save the URI: 566373416292.dkr.ecr.ap-south-1.amazonaws.com/waste

## 4. Create EC2 machine (Ubuntu)

## 5. Open EC2 and Install docker in EC2 Machine:

    #optinal

    sudo apt-get update -y

    sudo apt-get upgrade

    #required

    curl -fsSL https://get.docker.com -o get-docker.sh

    sudo sh get-docker.sh

    sudo usermod -aG docker ubuntu

    newgrp docker

# 6. Configure EC2 as self-hosted runner:

    setting>actions>runner>new self hosted runner> choose os> then run command one by one

# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app
