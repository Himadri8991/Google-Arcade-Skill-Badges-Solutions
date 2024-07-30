# Pub/Sub Lite: Qwik Start || [GSP832](https://www.cloudskillsboost.google/course_templates/728/labs/461594) ||

### Run the following Commands in CloudShell
### From "Task 1" you can find your REGION,
```
export REGION=
```

```
gcloud services enable pubsublite.googleapis.com

sleep 30

pip3 install --upgrade google-cloud-pubsublite



gcloud pubsub lite-topics create my-lite-topic \
          --zone=$REGION-a --partitions=1 \
          --per-partition-bytes=30GiB --message-retention-period=2w

gcloud pubsub lite-subscriptions create my-lite-subscription \
  --project=$DEVSHELL_PROJECT_ID \
  --zone=$REGION-a \
  --topic=my-lite-topic \
  --delivery-requirement=deliver-after-stored
echo "${CYAN}${BOLD}With Regards Himadri${RESET}"
```

# Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 
