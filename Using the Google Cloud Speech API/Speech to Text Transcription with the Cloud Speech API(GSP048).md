# Speech to Text Transcription with the Cloud Speech API || [GSP048](https://www.cloudskillsboost.google/course_templates/756/labs/475241) ||

### Run the following Commands in CloudShell

## Manual Steps:-
### To create an API key, click ```Navigation menu``` > ```APIs & services``` > ```Credentials```
### Then click ```Create credentials```
### In the drop down menu, select ```API key```
### Copy it

### Search ```VM instances``` > Connect ```SSH```

## Run the following Commands in *SSH*
```
export API_KEY=
```

```
cat > request.json <<EOF

{
  "config": {
      "encoding":"FLAC",
      "languageCode": "en-US"
  },
  "audio": {
      "uri":"gs://cloud-samples-data/speech/brooklyn_bridge.flac"
  }
}

EOF

curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json \
"https://speech.googleapis.com/v1/speech:recognize?key=${API_KEY}" > result.json

----------------------------------------------------------------------------------------------------------------------------------------------------

rm -f request.json

cat >> request.json <<EOF

 {
  "config": {
      "encoding":"FLAC",
      "languageCode": "fr"
  },
  "audio": {
      "uri":"gs://cloud-samples-data/speech/corbeau_renard.flac"
  }
}

EOF

curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json \
"https://speech.googleapis.com/v1/speech:recognize?key=${API_KEY}" > result.json
echo "${CYAN}${BOLD}With Regards Himadri${RESET}"
----------------------------------------------------------------------------------------------------------------------------------------------------
```
# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
