 # Get Started with Dataplex: Challenge Lab || [ARC117](https://www.cloudskillsboost.google/course_templates/726/labs/461571) ||

 
### Run the following Commands in CloudShell
### From "Challenge scenario" you can find your Region=LOCATION,

```
export LOCATION=
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

echo "${YELLOW}${BOLD}Starting${RESET}" "${GREEN}${BOLD}Execution${RESET}"

export ID=$DEVSHELL_PROJECT_ID

gcloud services enable datacatalog.googleapis.com
gcloud services enable dataplex.googleapis.com

gcloud dataplex lakes create customer-engagements \
   --location=$LOCATION \
   --display-name="Customer Engagements"

gcloud dataplex zones create raw-event-data \
    --location=$LOCATION \
    --lake=customer-engagements \
    --display-name="Raw Event Data" \
    --type=RAW \
    --resource-location-type=SINGLE_REGION \
    --discovery-enabled

gsutil mb -p $ID -c REGIONAL -l $LOCATION gs://$ID

gcloud dataplex assets create raw-event-files \
--location=$LOCATION \
--lake=customer-engagements \
--zone=raw-event-data \
--display-name="Raw Event Files" \
--resource-type=STORAGE_BUCKET \
--resource-name=projects/my-project/buckets/${ID}
echo "${CYAN}${BOLD}With Regards Himadri${RESET}"

#-----------------------------------------------------end----------------------------------------------------------#
```

### Task 3. Create and apply a tag template to a zone
## ```Click``` here: (https://console.cloud.google.com/dataplex/templates/create)

## From "Task 3" you can find your ```Template Name``` & ```LOCATION```,
### Template display name > Location

## From "Task 3" you can find your ```Field Name```,
### ADD A FIELD > Type ```Enumerated``` > Enumerated Values > Values 1 ```Y``` > ADD VALUES > Values 2 ```N``` > ```CREATE```


# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
