# Flask Hello App Deployment on Google Cloud App Engine

This guide explains how to deploy the Flask Hello application to Google Cloud App Engine using **Google Cloud Shell**.

---

## Prerequisites

Before starting, make sure you have:

- A Google Cloud account
- A Google Cloud project created
- Billing enabled
- App Engine API enabled

---

## Step 1: Open Google Cloud Shell

1. Login to Google Cloud Console
2. Click **Activate Cloud Shell** (top right terminal icon)

---

## Step 2: Clone the Repository

Run the following commands:

```bash
git clone https://github.com/preethihepsiba-cloud/flask-hello
cd flask-hello

Project Structure
flask-hello/
│
├── app.py
├── requirements.txt
├── app.yaml
└── templates/

---

## Step 3: Configure Google Cloud

Initialize gcloud and follow the prompts:

gcloud init

Select:

Google account

Project ID

Default region (if asked)

---

## Step 4: Initialize App Engine

Create App Engine application:

gcloud app create --region=us-central1

Choose region:

us-central1

---

##Step 5: Deploy the Application

Deploy the Flask application:

gcloud app deploy

Press Y when prompted.

---

##Step 6: Access Your Application

After deployment, open the application:

gcloud app browse

Or visit:

https://[PROJECT_ID].appspot.com

Replace [PROJECT_ID] with your Google Cloud Project ID.

---

##Step 7: Testing and Scaling
View Logs

Monitor logs in real time:

gcloud app logs tail -s default
Update Application

After making changes to the code:

gcloud app deploy
