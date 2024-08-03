# FitgenAI
### Building a fitness chatbot(FitGen AI) using GEMINI-1.5-PRO on the Google Cloud Platform (GCP). The chatbot will analyze workout routines and provide real-time, personalized feedback on posture and exercise techniques, helping users improve their workout efficiency and safety.The bot is re-trained on the recomendations and workout patterns, thereby providing better feed back.

### Documentation: For more detailed implemetation please refer to the blog
https://medium.com/@yakula7/how-to-build-a-personalized-fitness-chatbot-powered-by-gemini-on-google-cloud-platform-2c49041321b8

### function-source.zip : This folder contains code to run the google cloud storage trigger funtion. 
- main.py: Contains the code for cloud funtion trigger and getting the recomendations via gemini-1.5-pro into the firestore database.
- requirements.txt: contains all the necessary installations.

How to run? : in the GCP console select cloud funtion and use the options to create the cloud storage trigger function. Under bucket choose your respective cloud storage bucket.Once you have uploaded the codes, deploy the funtion  and check the logs for  errors.

![image](https://github.com/user-attachments/assets/d23d3e29-726a-4652-9f37-1b96ea242737)


### streamlit_deploy.zip:  This folder contains code to run the FitGen AI app in the cloud run

- main.py: Contains the code to deploy the app in the.
- requirements.txt: contain all the necessary installations.

How to run? : In the console open, Google app engine and click on open editor , use the code (main.py) and the requirements.txt, Dockerfile file to successfully pull the recommendations field from firestore data and feed it into Gemini-1.5-pro for personalized recommendation. Then, in the terminla make sure you navigate to the your project and the folder containing the
deploymnet code and run the following command

`gcloud run deploy - port=3000 - allow-unauthenticated - platform=managed - region=us-central1 - source=. –your-service-account , the app will be deployed via StreamLit`

### Demo
Once you have deployed the app successfully you can input your prompt and get receive personalized recommendations from your historical data with the help of GEMINI-1.5-pro on Streamlit.
https://cdn-images-1.medium.com/max/1600/1*Ab43lJzd_8wKwR4gtveTIQ.png![image](https://github.com/user-attachments/assets/0999559a-bd42-4117-8b5f-009a6ce55177)


