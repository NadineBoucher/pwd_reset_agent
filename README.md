This is a basic Google Cloud Conversational Agents for password reset.

It is build using Playbook and reference one tool openapi.


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

