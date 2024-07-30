# Pub/Sub: Qwik Start - Python || [GSP094](https://www.cloudskillsboost.google/course_templates/637/labs/464358) ||

### Run the following Commands in CloudShell
```
gcloud auth list 

sudo apt-get install -y virtualenv

python3 -m venv venv

source venv/bin/activate

pip install --upgrade google-cloud-pubsub

git clone https://github.com/googleapis/python-pubsub.git

cd python-pubsub/samples/snippets

python publisher.py -h

python publisher.py $GOOGLE_CLOUD_PROJECT create MyTopic

python subscriber.py $GOOGLE_CLOUD_PROJECT create MyTopic MySub
echo "${CYAN}${BOLD}With Regards Himadri${RESET}"
```

# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
