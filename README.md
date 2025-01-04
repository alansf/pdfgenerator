# Heroku-Salesforce Sample Integration App with Fastify.

# READ ME 

heroku create -a APP_NAME --org ORG_NAME

git push heroku main

heroku addons:create heroku-integration -a APP_NAME

heroku salesforce:connect ORG_NAME -l "https://login.salesforce.com" -a APP_NAME

heroku datacloud:connect ORG_NAME -l "https://login.salesforce.com" -a APP_NAME

heroku integration:connections

heroku salesforce:import api-spec.yaml -a APP_NAME -o ORG_NAME -c HerokuAPI
