# App Engine: Qwik Start - Python || [GSP067](https://www.cloudskillsboost.google/focuses/1014?parent=catalog) ||

### Run the following Commands in CloudShell

### From "Setup and requirement" you can find your REGION,
```
export REGION=
```
```
#!/bin/bash
# Define color variables

BLACK=`tput setaf 0`
RED=`tput setaf 1`
GREEN=`tput setaf 2`
YELLOW=`tput setaf 3`
BLUE=`tput setaf 4`
MAGENTA=`tput setaf 5`
CYAN=`tput setaf 6`
WHITE=`tput setaf 7`

BG_BLACK=`tput setab 0`
BG_RED=`tput setab 1`
BG_GREEN=`tput setab 2`
BG_YELLOW=`tput setab 3`
BG_BLUE=`tput setab 4`
BG_MAGENTA=`tput setab 5`
BG_CYAN=`tput setab 6`
BG_WHITE=`tput setab 7`

BOLD=`tput bold`
RESET=`tput sgr0`
#----------------------------------------------------start--------------------------------------------------#

echo "${BG_MAGENTA}${BOLD}Starting Execution${RESET}"

gcloud config set compute/region $REGION

gcloud services enable appengine.googleapis.com

git clone https://github.com/GoogleCloudPlatform/python-docs-samples.git

cd python-docs-samples/appengine/standard_python3/hello_world

sed -i 's/Hello World!/Hello, Cruel World!/g' main.py

gcloud app create --region=$REGION

yes | gcloud app deploy

echo "${BG_RED}${BOLD}Congratulations For Completing The Lab !!!${RESET}"

echo "${CYAN}${BOLD}With Regards Himadri${RESET}"
#-----------------------------------------------------end----------------------------------------------------------#
```

# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
