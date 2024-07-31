# App Engine: Qwik Start - Go || [GSP070](https://www.cloudskillsboost.google/focuses/2754?parent=catalog) ||

### Run the following Commands in CloudShell
### From "Task 1" you can find your REGION,
```
export REGION=
```
```
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

echo "${YELLOW}${BOLD}Starting${RESET}" "${GREEN}${BOLD}Execution${RESET}"

gcloud services enable appengine.googleapis.com

sleep 10

gcloud config set compute/region $REGION

git clone https://github.com/GoogleCloudPlatform/golang-samples.git

cd golang-samples/appengine/go11x/helloworld

sudo apt-get install google-cloud-sdk-app-engine-go
gcloud app deploy

echo "${RED}${BOLD}Congratulations${RESET}" "${WHITE}${BOLD}for${RESET}" "${GREEN}${BOLD}Completing the Lab !!!${RESET}"
echo "${CYAN}${BOLD}With Regards Himadri${RESET}"
#-----------------------------------------------------end----------------------------------------------------------#
```

# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
