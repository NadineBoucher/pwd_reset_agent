This is a basic Google Cloud Conversational Agents (Playbook using Gemini) for password reset.

Those assets are meant to be used as part of an enablement session, thus the limited instructions here.

Description:
- The agent greet the user and collect its full name
- Assuming the user say something like : "I need to reset my pwd, i got locked out of my account"
- The agent will also collect the last 4 digits of the user SSN and its billing zip code
- Call the Tool --> OpenAPI --> CF/Cloud Run to reset the pwd (dummy).

1. How to deploy a cloud function .zip using the command line?
https://cloud.google.com/functions/docs/deploy#basics

   For example: 
   
   gcloud functions deploy pwd_reset \
    --gen2 \
    --region=us-central1 \
    --runtime=python311 \
    --source=[Enter your location here] \
    --entry-point=pwd_reset

 

2. How to import the provided agent?
- Create a new Conversational Agent, see here: https://cloud.google.com/dialogflow/cx/docs/quick/build-agent-playbook#create_the_agent
- then import the .zip agent provided (this will overwrite the agent previously created).



3. Using the workshop_faqs.csv create a simple FAQ DS and attach it to the agent.
- See here for more details: https://cloud.google.com/dialogflow/cx/docs/concept/data-store#faq


