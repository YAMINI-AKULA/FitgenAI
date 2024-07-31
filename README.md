# FitgenAI
This repo consists of code to implement an end-to-end Fitness chatbot using Gemini on GCP platform.

function-source.zip : This folder contains code to run the google cloud storage trigger funtion. 
main.py: Contains the code for cloud funtion trigger and getting the recomendations via gemini-1.5-pro into the firestore database.
requirements.txt: contain all the necessary installations.

How to run? : in the GCP console select cloud funtion and use the options to create the cloud storage trigger function. Under bucket choose your respective cloud storage bucket.Once you have uploaded the codes, deploy the funtion  and check the logs for  errors.

streamlit_deploy.zip:  This folder contains code to run the FitGen AI app in the cloud run

main.py: Contains the code to deploy the app in the.
requirements.txt: contain all the necessary installations.

How to run? : In the console open, Google app engine and click on open editor , use the code (main.py) and the requirements.txt, Dockerfile file to successfully pull the recommendations field from firestore data and feed it into Gemini-1.5-pro for personalized recommendation. Then, in the terminla make sure you navigate to the your project and the folder containing the
deploymnet code and run the following command gcloud run deploy - port=3000 - allow-unauthenticated - platform=managed - region=us-central1 - source=. –your-service-account , the app will be deployed via StreamLit

