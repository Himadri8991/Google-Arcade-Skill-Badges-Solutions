# Cloud Storage: Qwik Start - Cloud Console || [GSP073](https://www.cloudskillsboost.google/course_templates/658/labs/464084) ||

### Run the following Commands in CloudShell

### From "Task 1" you can find your REGION,
```
export REGION=
```
```
gcloud config set compute/region $REGION

gsutil mb gs://$DEVSHELL_PROJECT_ID

curl https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Ada_Lovelace_portrait.jpg/800px-Ada_Lovelace_portrait.jpg --output ada.jpg

mv ada.jpg kitten.png

gsutil cp kitten.png gs://$DEVSHELL_PROJECT_ID

gsutil cp -r gs://$DEVSHELL_PROJECT_ID/kitten.png .

gsutil cp gs://$DEVSHELL_PROJECT_ID/kitten.png gs://$DEVSHELL_PROJECT_ID/image-folder/

gsutil iam ch allUsers:objectViewer gs://$DEVSHELL_PROJECT_ID
echo "${CYAN}${BOLD}With Regards Himadri${RESET}"
#-----------------------------------------------------end----------------------------------------------------------#
```

# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
