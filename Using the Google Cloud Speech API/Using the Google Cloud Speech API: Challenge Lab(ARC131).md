# Using the Google Cloud Speech API: Challenge Lab || [ARC131](https://www.cloudskillsboost.google/focuses/65993?parent=catalog) ||

## [Manual Steps](https://console.cloud.google.com/apis/credentials) :-
### To create an API key, click ```Navigation menu``` > ```APIs & services``` > ```Credentials```
### Then click ```Create credentials```
### In the drop down menu, select ```API key```
### Copy it

### Search ```VM instances``` > Connect ```SSH```

## Run the following Commands in *SSH*
```
export API_KEY=
export REQUEST1=
export RESPONSE1=
export REQUEST2=
export RESPONSE2=
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

cat > "$REQUEST1" <<EOF
{
  "config": {
    "encoding": "LINEAR16",
    "languageCode": "en-US",
    "audioChannelCount": 2
  },
  "audio": {
    "uri": "gs://spls/arc131/question_en.wav"
  }
}
EOF

curl -s -X POST -H "Content-Type: application/json" --data-binary @"$REQUEST1" \
"https://speech.googleapis.com/v1/speech:recognize?key=$API_KEY" > $RESPONSE1

cat > "$REQUEST2" <<EOF
{
  "config": {
    "encoding": "FLAC",
    "languageCode": "es-ES"
  },
  "audio": {
    "uri": "gs://spls/arc131/multi_es.flac"
  }
}
EOF

curl -s -X POST -H "Content-Type: application/json" --data-binary @"$REQUEST2" \
"https://speech.googleapis.com/v1/speech:recognize?key=$API_KEY" > $RESPONSE2

echo "${RED}${BOLD}Congratulations${RESET}" "${WHITE}${BOLD}for${RESET}" "${GREEN}${BOLD}Completing the Lab !!!${RESET}"
echo "${CYAN}${BOLD}With Regards Himadri${RESET}"
```

# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
