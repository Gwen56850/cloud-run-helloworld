Hello world
============================

The goal of this repo is to deploy to Google Cloud Run a dockerised Hello world 

Build the container image using Cloud Build, by running the following command from the directory containing the Dockerfile:

* dev  
    `gcloud builds submit --tag gcr.io/tidy-ivy-127308/helloworld`
    
This need to be done only once. The image is stored in Container Registry and can be re-used if desired.

Deploying to Cloud Run

* dev  
    `gcloud run deploy --image gcr.io/tidy-ivy-127308/helloworld --platform managed`
    
Access the UI

* dev  
    The URL is displayed in the console https://console.cloud.google.com/run/detail/europe-west1/helloworld/metrics?project=tidy-ivy-127308
    
    