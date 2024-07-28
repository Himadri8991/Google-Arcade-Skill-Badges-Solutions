# Classify Images with TensorFlow on Google Cloud: Challenge Lab || [GSP398](https://www.cloudskillsboost.google/course_templates/646/labs/476328) ||

### Run the following Commands in CloudShell
### *Copy the Zone from the lab panel,
```
export ZONE=
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

gcloud services enable \
  compute.googleapis.com \
  monitoring.googleapis.com \
  logging.googleapis.com \
  notebooks.googleapis.com \
  aiplatform.googleapis.com \
  artifactregistry.googleapis.com \
  container.googleapis.com

export NOTEBOOK_NAME="cnn-challenge"
export MACHINE_TYPE="e2-standard-2"

gcloud notebooks instances create $NOTEBOOK_NAME \
  --location=$ZONE \
  --vm-image-project=deeplearning-platform-release \
  --vm-image-family=tf-2-11-cu113-notebooks \
  --machine-type=$MACHINE_TYPE

echo "${RED}${BOLD}With Regards Himadri${RESET}"

#-----------------------------------------------------end----------------------------------------------------------#
```
## Next Step..
* Go to `User-managed Notebooks` from [here](https://console.cloud.google.com/vertex-ai/workbench/user-managed?)

## Open Terminal
### Run the following Commands in Terminal
```
git clone https://github.com/GoogleCloudPlatform/training-data-analyst
```
## training-data-analyst > self-paced-labs > learning-tensorflow > cnn_challenge_lab 
### Delete the file ``` cnn_challenge_lab.ipynb ```

### Download `Jupyter` file from [here](https://github.com/Himadri8991/Google-Arcade-Skill-Badges-Solutions/blob/ba0387b88f06cdbacdb5e578df5ef339afd70197/Classify%20Images%20with%20TensorFlow%20on%20Google%20Cloud/Classify%20Images%20with%20TensorFlow%20on%20Google%20Cloud%3A%20Challenge%20Lab/cnn_challenge_lab.ipynb)


## Upload the file ``` cnn_challenge_lab.ipynb ```
* Run > Run all cell

### If Kernel becomes stopped, *You have to Run Again* by:- 
* Run > Run Selected cell and all Below









### Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
