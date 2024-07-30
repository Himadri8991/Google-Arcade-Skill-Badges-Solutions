 # Cloud IAM: Qwik Start || [GSP064](https://www.cloudskillsboost.google/course_templates/637/labs/464352) ||

## Open Google Console with USERNAME-1

### Run the following Commands in CloudShell

### From "Lab Panel" you can find your USERNAME_2,
```
export USERNAME_2=
```
```
gsutil mb -l us -b on gs://$DEVSHELL_PROJECT_ID

echo "subscribe to quicklab " > sample.txt

gsutil cp sample.txt gs://$DEVSHELL_PROJECT_ID

gcloud projects remove-iam-policy-binding $DEVSHELL_PROJECT_ID \
  --member=user:$USERNAME_2 \
  --role=roles/viewer

gcloud projects add-iam-policy-binding $DEVSHELL_PROJECT_ID \
  --member=user:$USERNAME_2 \
  --role=roles/storage.objectViewer

echo "${CYAN}${BOLD}With Regards Himadri${RESET}"
```

# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
